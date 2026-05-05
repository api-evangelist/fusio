---
title: "Fusio 6.0 released"
url: "https://www.fusio-project.org/blog/fusio-6.0-released"
date: "2025-09-06T14:30:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We are really proud to announce the next major version 6.0 of Fusio. This release is a great milestone for Fusio,
with the new connection panels you can build now complete APIs within Fusio without the need to use an external tool.
Through the <abbr title="Model Context Protocol">MCP</abbr> support there are now also many exciting possibilities
how you can interact with Fusio. Our goal is to develop a platform which helps everybody to build great APIs.
As usual the following list covers all important features of this release:</p>

<ul>
    <li>
        <b>Added MCP server <a href="https://github.com/apioo/fusio/issues/626">#626</a></b>
        <p>We have added an MCP server, it is possible to use the MCP server directly through stdio transport by using the <code>php bin/fusio mcp</code> command.
        There is also an experimental HTTP transport which you need to activate through the configuration.</p>
    </li>
    <li>
        <b>Improved API documentation</b>
        <p>To help LLMs understand our API we have added many descriptions to each operation and schema, which in the end now also help developers.</p>
    </li>
    <li>
        <b>Added OAuth2 authorization server <a href="https://github.com/apioo/fusio/issues/245">#245</a></b>
        <p>Fusio includes now a small OAuth2 authorization server which can be used to obtain an access token. This OAuth2 server can also be used by
        external apps i.e. if you use Fusio as backend for your single page application.</p>
    </li>
    <li>
        <b>Added Fusio identity provider to use the internal authorization server</b>
        <p>All internal apps now also automatically register the authorization server as identity provider so you can use it to login.
        In the future we may move completely to this authorization server.</p>
    </li>
    <li>
        <b>Added well-known oauth protected resource endpoint <a href="https://datatracker.ietf.org/doc/html/rfc9728">RFC9728</a></b>
        <p>To handle authentication with MCP we have implemented the oauth protected resource endpoint RFC.</p>
    </li>
    <li>
        <b>Add backend filesystem, http and sdk API and panel <a href="https://github.com/apioo/fusio/issues/609">#609</a></b>
        <p>We have added new designer panels for different connection types, i.e. the HTTP panel allows to execute HTTP requests and the filesystem panel allows to manage files.</p>
    </li>
    <li>
        <b>Moved backend database endpoint under connection (breaking change)</b>
        <p>We have moved the complete database endpoint under the connection which now works similar to the other connection designer panels. Note this is a breaking API change,
        so you need to adjust your URLs in case you use this endpoint. Basically you only need to change the base path from <code>/backend/database/:connection_id</code> to
        <code>/backend/connection/:connection_id/database</code>.</p>
    </li>
    <li>
        <b>Add option to configure different captcha provider</b>
        <p>It is now possible to configure different captcha provider so that you can use an alternative to ReCaptcha. The captcha is used to protect your user registration.</p>
    </li>
    <li>
        <b>Add config option to disable user registration</b>
        <p>In case you want to build an internal app you can deactivate the user registration.</p>
    </li>
    <li>
        <b>Improve responsive design of the backend app</b>
        <p>We have improved the backend CSS layout so that it is more responsive for other devices like a tablet or smartphone.</p>
    </li>
</ul>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page. For more details and background information about the release you can also
take a look at <a href="https://chrisk.app/blog/fusio-6.0-released">my personal blog</a>, where I have published a post about the new 6.0 release.</p>

<p>Best regards<br />
Christoph</p>
