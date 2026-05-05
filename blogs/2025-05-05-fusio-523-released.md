---
title: "Fusio 5.2.3 released"
url: "https://www.fusio-project.org/blog/fusio-5.2.3-released"
date: "2025-05-05T18:22:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We like to announce the next version 5.2.3 of Fusio. The following list covers all important features of this
release:</p>

<ul>
    <li>
        <b>Add option to set user points via API <a href="https://github.com/apioo/fusio/issues/586">#586</a></b>
        <p>It is now possible to set user points through the API which allows you to configure the user points through an external billing system.</p>
    </li>
    <li>
        <b>Added firewall feature <a href="https://github.com/apioo/fusio/issues/508">#508</a> <a href="https://github.com/apioo/fusio/issues/154">#154</a></b>
        <p>A new firewall feature was added, through this it is possible to block specific IPs from accessing your API. It includes also an automatic
        fail2ban logic to automatically ban specific IPs in case they have produced to many error responses.</p>
    </li>
    <li>
        <b>Add verbose mode to marketplace env/install/upgrade command for debugging <a href="https://github.com/apioo/fusio/issues/625">#625</a></b>
        <p>It is now possible to use the <code>-v</code> flag at the env/install/upgrade command to get more detailed error responses.</p>
    </li>
    <li>
        <b>Add CLI option to ready payload from stdin</b>
        <p>Besides providing data as argument or via a file it is now possible to read data from stdin by using "-" as argument.</p>
    </li>
    <li>
        <b>Updated marketplace env command, add an option to replace all available apps</b>
        <p>The env command has now an option replace env variables for all available apps at the <code>apps/</code> folder, this is now also used at the docker
        image so that it is possible to add additional apps to the docker image.</p>
    </li>
</ul>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
