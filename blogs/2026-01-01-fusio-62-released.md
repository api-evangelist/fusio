---
title: "Fusio 6.2 released"
url: "https://www.fusio-project.org/blog/fusio-6.2-released"
date: "2026-01-01T16:29:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 6.2 of Fusio. The largest change of this release is the backend migration from
<a href="https://angular.dev/">Angular</a> 18 to 20. This affects the Angular SDK, TypeSchema editor and backend app, in
the process we have also updated many dependencies like the <a href="https://microsoft.github.io/monaco-editor/">Monaco</a>
editor and <a href="https://apexcharts.com/">Apexcharts</a>. All components of the backend app are now standalone, and
we use the new <code>@for</code> <code>@if</code> syntax and signals for input and output. This makes the backend app
fit for future Angular releases, and we also benefit from all changes in the ecosystem. Since this is a larger rewrite
of the backend feel free to <a href="https://github.com/apioo/fusio/issues">open an issue</a> in case you have found a
problem. The following list covers all important features of this release:</p>

<ul>
    <li>
        <b>Migrate backend app from Angular 18 to 20</b>
        <p>The backend app was migrated from Angular 18 to 20 using new language features and updating all dependencies.</p>
    </li>
    <li>
        <b>Added backend code editor view and improved code completion</b>
        <p>We have implemented a new code editor view to develop actions.</p>
        <div class="mt-4 mb-4 text-center">
            <img alt="Action Designer Editor" class="img-fluid" src="/img/blog/fusio-6.2-released/action_designer_editor.png" />
        </div>
        <p>This view is dedicated to the Worker actions and improves the development experience for users who like to
        use the backend. The editor has now more space and on the right side panel you can select a connection to get
        additional information about this connection. While developing an action you often need to use an existing
        connection i.e. select data from a table or access a remote API. This side panel provides more information like
        available methods, and we also show details if available, i.e. for a database connection we list available tables
        on the connection. Besides this we have also improved the code completion of the editor.</p>
    </li>
    <li>
        <b>Backend use schema editor</b>
        <p>To create and update a schema we now use everywhere the schema editor. Previously there was a JSON editor
        where a user could provide a raw <a href="https://typeschema.org/">TypeSchema</a> specification but this is now
        replaced with the editor since it is much easier for new users to create a schema.</p>
        <div class="mt-4 mb-4 text-center">
            <img alt="Schema Editor" class="img-fluid" src="/img/blog/fusio-6.2-released/schema_editor.png" />
        </div>
        <p>We use this editor already in many projects and it helps to improve the user experience. The editor has also
        an import option so if the user likes to provide a raw TypeSchema specification this is still possible.</p>
    </li>
    <li>
        <b>Add marketplace bundle</b>
        <p>At the marketplace we have introduced a new bundle concept. A bundle is basically a set of Fusio entities
        like i.e. an action or schema. You can create a bundle to share such entities with our community. With this
        new option you can now create a bundle at your local Fusio installation and submit these entities to the
        marketplace.</p>
        <div class="mt-4 mb-4 text-center">
            <img alt="Bundle Details" class="img-fluid" src="/img/blog/fusio-6.2-released/bundle_details.png" />
        </div>
        <p>Basically a bundle contains a reference to your local entities and if you submit the bundle to the
        marketplace Fusio will convert those references into a fitting object. A third user can then install this bundle
        from the marketplace. You need to <a href="https://www.fusio-project.org/marketplace">register</a>
        at the marketplace, and then you can provide your credentials at your local Fusio installation under
        System / Config (<code>marketplace_client_id</code> / <code>marketplace_client_secret</code>).</p>
        <p>This is only a soft launch of this new concept, but in the future users could use this marketplace to create
        a vibrant community to share such entities. This would work similar to platforms like
        <a href="https://zapier.com/">Zapier</a> where users can share existing actions to solve or automate a specific
        task but in the open-source and self-hosted spirit.</p>
    </li>
    <li>
        <b>HTTP-Raw Action GET Error - Template "body" is not defined in HTTP <a href="https://github.com/apioo/fusio/issues/659">#659</a></b>
        <p>The body parameter is no longer required.</p>
    </li>
    <li>
        <b>Remove FQDN from OAuth2 username <a href="https://github.com/apioo/fusio/issues/655">#655</a></b>
        <p>When normalizing OAuth2 usernames we automatically remove the @ part.</p>
    </li>
    <li>
        <b>Added new requests per ip, operation and user statistic</b>
        <p>We have added some new statistics to see the request count by ip, operations and user.</p>
    </li>
    <li>
        <b>Migrate from psalm to phpstan</b>
        <p>Internally we have migrated the Fusio backend implementation and many libraries from <a href="https://psalm.dev/">Psalm</a>
        to <a href="https://phpstan.org/">PHPStan</a>.</p>
    </li>
</ul>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
