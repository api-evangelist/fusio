---
title: "Fusio 5.2.5 released"
url: "https://www.fusio-project.org/blog/fusio-5.2.5-released"
date: "2025-06-21T21:33:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 5.2.5 of Fusio. The following list covers all important features of this
release:</p>

<ul>
    <li>
        <b>Upgrade command use resources path</b>
        <p>The upgrade command to migrate YAML operations to PHP is now using the resource path from the config.</p>
    </li>
    <li>
        <b>App detect url via javascript for localhost</b>
        <p>For a long time we had the problem, that once you have installed an app and changed the url later on, your apps would no longer work
        since we could not update the url from the already installed app. To solve this problem we use now the JavaScript <code>location.hostname</code>
        to dynamically get the host in case no url is configured. This means for new installations the <code>APP_URL</code> and <code>APP_APPS_URL</code>
        environment variables are optional.</p>
    </li>
    <li>
        <b>Implement API Catalog <a href="https://www.rfc-editor.org/rfc/rfc9727.html">RFC9727</a></b>
        <p>We have implemented the new API Catalog RFC which helps to make your APIs more discoverable.</p>
    </li>
    <li>
        <b>Add humans.txt and robots.txt</b>
        <p>The <code>/humans.txt</code> and <code>/robots.txt</code> endpoint are now implemented and served directly from Fusio.</p>
    </li>
    <li>
        <b>Added the following .well-known/ uris: api-catalog, oauth-authorization-server and security.txt</b>
        <p>We implemented various useful <code>.well-known/</code> endpoints.</p>
    </li>
    <li>
        <b>Fix redoc app handle dynamic urls</b>
        <p>For the redoc app the dynamic url handling has not worked since the url was not executed in a JavaScript context which is now fixed.</p>
    </li>
    <li>
        <b>Fix WorkerPHPLocal action cache path</b>
        <p>The local PHP worker now uses the correct cache path and therefore writes the action code into the <code>cache/</code> folder.</p>
    </li>
    <li>
        <b>Removed introspection from database connections</b>
        <p>The introspection feature is replaced by the database panel which allows a user to access the db. Because of this, we have removed the
        implementation and marked the interface as deprecated. Please do no longer use this interface inside your custom action.</p>
    </li>
</ul>

<p>For the next 5.3 release, we are thinking about implementing a custom <a href="https://github.com/apioo/fusio/issues/626">MCP server</a> inside
Fusio. This means all your operations could be used as tool from an LLM. Please let us know whether you are also interested in such a use-case.</p>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
