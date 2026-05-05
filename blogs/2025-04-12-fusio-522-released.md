---
title: "Fusio 5.2.2 released"
url: "https://www.fusio-project.org/blog/fusio-5.2.2-released"
date: "2025-04-12T19:07:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 5.2.2 of Fusio. The following list covers all important features of this
release:</p>

<ul>
    <li>
        <b>Add form feature to build Forms for your API endpoints</b>
        <p>We have added a new "Form" panel at the backend. The form panel should help users to build a simple
        UI for an API endpoint. I.e. if you have created a "Product" API and you need a simple way to create a form for
        this endpoint so that users can create product entries. At the core to create a new form you need to select an operation and
        specific an UI schema.</p>
        <div class="mt-4 mb-4 text-center">
            <img alt="Form panel" class="img-fluid" src="/img/blog/fusio-5.2.2-released/form-panel.png" />
        </div>
        <p>The UI schema is basically an arbitrary JSON to describe the form, this format depends on the used frontend form library
        i.e. we could use <a href="https://github.com/eclipsesource/jsonforms">JSON Forms</a>. We can then request the
        <code>/consumer/form/~my-test-form</code> endpoint to get our form including the UI and JSON Schema of the operation, the JSON
        Schema is automatically generated from the incoming schema of the selected operation. In this first step we have added the form
        panel to the backend, but we also plan to create a dedicated "form" app where users can login to directly work with those forms.</p>
    </li>
    <li>
        <b>Add option to configure trusted IP header for proxy</b>
        <p>It is now possible to configure a trusted IP header proxy. This is needed in case you Fusio instance runs behind a proxy
        so that our rate limiting service gets the actual IP of the user, otherwise all request come from the same IP and you quickly
        get 429 responses. It is important to set an actual trusted header otherwise a user would be able to provide a random IP through
        the header.</p>
    </li>
    <li>
        <b>Add command to migrate YAML definitions to PHP</b>
        <p>We have adjusted the <code>system:upgrade</code> command to migrate a YAML definition to PHP. This is completely optional
        but it can be useful for better type-safety of your operation configuration.</p>
        <pre><code>php bin/fusio system:upgrade</code></pre>
    </li>
    <li>
        <b>Add OpenAI SDK integration</b>
        <p>We have added a new OpenAI SDK which can be used to talk to the OpenAI API.</p>
    </li>
    <li>
        <b>Improved docker handling in case the marketplace is down</b>
        <p>In the last week we had some performance problems with our marketplace server, also due to some DDOS requests which we have
        received. This should be now mitigated but we have also improved the code so that the docker build should always start even
        in case the marketplace server is down.</p>
    </li>
    <li>
        <b>Fixed scope list empty #620</b>
        <p>We have updated the backend, developer and account app to the latest version so that the new token scope selection form
        works as expected.</p>
    </li>
</ul>

<p>Internally we are working also on a new project called Fusio Plant which is basically an API driven server panel to easily self-host
apps on your server, similar to server panels like cPanel, Plesk or Webmin. It is dedicated to easily run multiple Fusio instances on your
server, but it can be also used to run other apps.</p>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
