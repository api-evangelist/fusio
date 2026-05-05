---
title: "Fusio 6.3 released"
url: "https://www.fusio-project.org/blog/fusio-6.3-released"
date: "2026-02-01T10:28:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>We are happy to announce the release of Fusio 6.3. This version introduces a new AI adapter and agent connection,
which allows you to connect to remote agents. These agents can help answer general questions about your Fusio instance
and assist in building custom endpoint logic and schemas.</p>

<p>The adapter and AI features are based on the new <a href="https://ai.symfony.com/">Symfony AI</a> components. All AI
features are optional and still experimental, but we wanted to make them available early to gather feedback from our
users. You can find more information about these features at our <a href="https://docs.fusio-project.org/docs/ai/">AI
documentation</a> page.

<p>The following list covers the most important changes in this release:</p>

<ul>
    <li>
        <b>Add AI adapter and agent connection <a href="https://github.com/apioo/fusio/issues/657">#657</a></b>
        <p>We have implemented a new <a href="https://github.com/apioo/fusio-adapter-ai">AI-Adapter</a> based on the
        Symfony AI components, which exposes an agent connection. This agent connection can be used in the Agent Designer,
        but you can also use it directly in your custom endpoints. A powerful feature is that all Fusio operations are
        available as tools that can be used by an agent. This allows the AI to interact directly with your Fusio
        instance in a controlled way.</p>
    </li>
    <li>
        <b>Add agent designer which allows to build actions using an agent connection</b>
        <p>The new Agent Designer allows you to build custom action logic through a simple conversational prompt. To get
        a first impression, take a look at the following screenshot:</p>
        <div class="mt-4 mb-4 text-center">
            <img alt="Agent Designer" class="img-fluid" src="/img/blog/fusio-6.3-released/agent_designer.png" />
        </div>
        <p>On the left, you see a chat-style prompt similar to what you know from other LLM providers. When the LLM
        returns a response, Fusio parses the generated code and loads it directly into the editor on the right.</p>
        <p>You can load code from previous prompts using the blue “Generated code” button. Once the code is inside the
        editor, you can execute it using the “Execute” button, which shows the response of the action. This allows you
        to quickly test whether the AI-generated code works as expected.</p>
    </li>
    <li>
        <b>Migrate from logiscape/mcp-sdk-php to mcp/sdk <a href="https://github.com/apioo/fusio/issues/651">#651</a></b>
        <p>We have switched our internal MCP library to the official MCP <a href="https://github.com/modelcontextprotocol/php-sdk">PHP SDK</a>.</p>
    </li>
    <li>
        <b>Action execution wrapped in transaction</b>
        <p>In the backend, it is possible to test an action by executing it through the Action Designer. This same logic
        is used in the Agent Designer when executing an action. To avoid side effects during testing, action execution
        is now wrapped in a transaction that is always rolled back. This means it is no longer possible, for example, to
        accidentally insert database entries while testing an action.</p>
    </li>
    <li>
        <b>Add response factory "proxy" method which returns a PSR response</b>
        <p>We have added a new proxy method to the response factory, which simplifies proxy scenarios where you only
        want to forward the response of an HTTP request.</p>
    </li>
    <li>
        <b>Improve HTTP adapter proxy performance</b>
        <p>Internally, Fusio now also uses the new proxy method, which improves performance.</p>
    </li>
</ul>

<p>If you want to provide some feedback take a look at our GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or
<a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
