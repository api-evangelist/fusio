---
title: "Introducing the new trigger system"
url: "https://www.fusio-project.org/blog/introducing-the-new-trigger-system"
date: "2025-10-11T10:00:00Z"
author: "chriskapp"
feed_url: "https://www.fusio-project.org/feed"
---
<p>With the latest 6.1 version we have introduced a new trigger system. The trigger system basically provides a way
to execute a specific action in case an event was dispatched. We have now three ways to execute an action, first through
an operation (HTTP request), then through a cronjob (periodically) and now through a custom event. If we take a look
at the Fusio <a href="https://docs.fusio-project.org/docs/bootstrap#architecture-overview">architecture</a>
the system is now build on the following entities.</p>

<div class="mt-4 mb-4 text-center">
    <img alt="Fusio Architecture" class="img-fluid" src="https://docs.fusio-project.org/assets/images/architecture_small-eddffeb37f5e15ae4e04abfa3e9b4668.png" width="500" />
</div>

<p>The trigger allows us to build actions which only execute a simple task and then dispatch an event.
Through the cronjob we can build actions which are periodically invoked which can be used i.e. to observe
a specific endpoint and only fire an event if specific conditions are met. Through this we can build <a href="https://zapier.com/">Zapier</a>
like workflows where we have a trigger and an action.</p>

<p>To create a trigger at the backend you only need to select the event and action which should be executed.</p>

<div class="mt-4 mb-4 text-center">
    <img alt="Trigger create" class="img-fluid" src="/img/blog/introducing-the-new-trigger-system/trigger-create.png" />
</div>

<p>To dispatch an event you can use the dispatcher which is available at every action. For example, you could use the
WorkerPHP action to run the following action which dispatches an event.</p>

<div class="mt-4 mb-4 text-center">
    <img alt="Action trigger event" class="img-fluid" src="/img/blog/introducing-the-new-trigger-system/trigger-action.png" />
</div>

<p>The trigger system is a powerful tool to build more decoupled actions which only solve a specific task and which together
compose more complex systems. We are also planing to improve our marketplace so that it is easier to share these kinds
of triggers and actions. So feel free to test this new feature and if you want to provide some feedback take a look at our
GitHub <a href="https://github.com/apioo/fusio/discussions">discussions</a> or <a href="https://github.com/apioo/fusio/issues">issues</a> page.</p>

<p>Best regards<br />
Christoph</p>
