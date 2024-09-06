[Learn about vector caching](./server/storage/vector-cache/VECTOR_CACHE.md)

## Telemetry & Privacy

AnythingLLM by Mintplex Labs Inc contains a telemetry feature that collects anonymous usage information.

<details>
<summary><kbd>More about Telemetry & Privacy for AnythingLLM</kbd></summary>

### Why?

We use this information to help us understand how AnythingLLM is used, to help us prioritize work on new features and bug fixes, and to help us improve AnythingLLM's performance and stability.

### Opting out

Set `DISABLE_TELEMETRY` in your server or docker .env settings to "true" to opt out of telemetry. You can also do this in-app by going to the sidebar > `Privacy` and disabling telemetry.

### What do you explicitly track?

We will only track usage details that help us make product and roadmap decisions, specifically:

- Typ of your installation (Docker or Desktop)
- When a document is added or removed. No information _about_ the document. Just that the event occurred. This gives us an idea of use.
- Type of vector database in use. Let's us know which vector database provider is the most used to prioritize changes when updates arrive for that provider.
- Type of LLM in use. Let's us know the most popular choice and prioritize changes when updates arrive for that provider.
- Chat is sent. This is the most regular "event" and gives us an idea of the daily-activity of this project across all installations. Again, only the event is sent - we have no information on the nature or content of the chat itself.

You can verify these claims by finding all locations `Telemetry.sendTelemetry` is called. Additionally these events are written to the output log so you can also see the specific data which was sent - if enabled. No IP or other identifying information is collected. The Telemetry provider is [PostHog](https://posthog.com/) - an open-source telemetry collection service.

[View all telemetry events in source code](https://github.com/search?q=repo%3AMintplex-Labs%2Fanything-llm%20.sendTelemetry\(&type=code)

</details>
