---
title: "Fusio 6.1 released"
url: "https://www.fusio-project.org/blog/fusio-6.1-released"
date: "2025-10-10T12:30:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 6.1 of Fusio. This release introduces a new trigger concept and
we have implemented the JsonRPC and GraphQL protocol which help to use Fusio in different environments.
The great thing about these new protocols is that our users get this JsonRPC or GraphQL support for free,
there is no need to change anything, since we expose only the existing operations. We now experience the
advantages of our operation based approach from our past decisions.
The following list covers all important features of this release:</p>

<ul>
    <li>
        <b>Added new trigger concept to invoke an action through an event <a href="https://github.com/apioo/fusio/issues/359">#359</a></b>
        <p>It is now possible to define a trigger, a trigger invokes an action in case an event occurs.
        This allows to decouple logic in your actions, for example you could create an action <code>fetch-latest-news</code> which triggers an event
        and an action <code>send-news-per-mail</code> which sends the actual news per mail and through a trigger you could invoke this action.
        Decoupling this is a really powerful way to build more complex systems.</p>
    </li>
    <li>
        <b>Added JsonRPC server <a href="https://github.com/apioo/fusio/issues/650">#650</a></b>
        <p>We have implemented a <a href="https://www.jsonrpc.org/">JsonRPC</a> server which can be used to invoke every operation through JsonRPC.
        JsonRPC is a great simple protocol which is widely used i.e. at BitCoin (and crypto in general), <a href="https://microsoft.github.io/language-server-protocol/">LSP</a>
        or <a href="https://modelcontextprotocol.io/">MCP</a>. For most cases we recommend to use REST API endpoints but in some circumstances
        it could be beneficial to use JsonRPC. At your API the endpoint is available at <code>/jsonrpc</code>. To use this endpoint you need to enable
        the JsonRPC server at the configuration.php file s. <code>fusio_jsonrpc</code> by default this is disabled.</p>
    </li>
    <li>
        <b>Added GraphQL server <a href="https://github.com/apioo/fusio/issues/649">#649</a></b>
        <p>We have implemented a <a href="https://graphql.org/">GraphQL</a> server which provides a way to invoke an operation through GraphQL.
        Our GraphQL implementation is readonly this means you can use it only to query data, mutations are not supported. We expose every
        GET operation as query which can be used at a frontend to create custom views. If your action gets invoked through GraphQL the action
        receives a GraphQL context which contains also all fields from the query so you could also adjust the actual query. At your API the endpoint
        is available at <code>/graphql</code>. To use this endpoint you need to enable the GraphQL server at the configuration.php
        file s. <code>fusio_graphql</code> by default this is disabled.</p>
    </li>
    <li>
        <b>Added OIDC discovery <a href="https://github.com/apioo/fusio/issues/648">#648</a></b>
        <p>We have added the <code>/.well-known/openid-configuration</code> endpoint which helps to automatically discover the OpenID configuration.</p>
    </li>
    <li>
        <b>Implemented OpenRPC specification <a href="https://github.com/apioo/fusio/issues/306">#306</a></b>
        <p>Since we have now JsonRPC support we have also implemented the <a href="https://open-rpc.org/">OpenRPC</a> specification which basically
        describes all available operations and types.</p>
    </li>
    <li>
        <b>Updated handling of public operations with invalid access token</b>
        <p>Previously if you have provided an invalid access token for a public endpoint you would get an error message, now we still allow the access to public endpoints
        even if the access token is invalid, since the request would work without access token.</p>
    </li>
    <li>
        <b>Possibility to configure SDKgen credentials at settings</b>
        <p>At the system setting it is now possible to configure the <a href="https://sdkgen.app/">SDKgen</a> credentials.</p>
    </li>
    <li>
        <b>Add option to resend the user activation code <a href="https://github.com/apioo/fusio/issues/642">#642</a></b>
        <p>At the user details there is now a new button to resend the activation code.</p>
    </li>
</ul>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
