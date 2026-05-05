---
title: "Fusio 5.2.4 released"
url: "https://www.fusio-project.org/blog/fusio-5.2.4-released"
date: "2025-06-12T09:28:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 5.2.4 of Fusio. The following list covers all important features of this
release:</p>

<ul>
    <li>
        <b>Update apps list</b>
        <p>We have updated the design of the app list script in the apps/ folder.</p>
    </li>
    <li>
        <b>Improve base url detection without defining a url</b>
        <p>Fusio now tries to auto-detect the url of your server by using the Host header in case no url was configured. Previously it was required to provide the url.</p>
    </li>
    <li>
        <b>Exclude firewall and rate-limit on deploy and testing</b>
        <p>The firewall was excluded from internal deployment and testing so that you don't get a ban in case of errors.</p>
    </li>
    <li>
        <b>Add schema nullable handling</b>
        <p>It is now possible to use the <code>nullable</code> attribute at your schema which allows making properties mandatory in case they are <code>nullable: false</code>, by default every property is nullable.</p>
    </li>
    <li>
        <b>Remove trailing slash from OpenAPI specification</b>
        <p>On OpenAPI generation we have removed the trailing slash of the base url.</p>
    </li>
</ul>

<p>With this release, we have also updated our website and readme to help new users start with Fusio.</p>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
