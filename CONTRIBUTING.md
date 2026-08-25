# Contributing

Document behavior at the level needed for a new Besu developer to understand the control flow. Do not list every method.

For each flow, identify the trigger, entry point, important calls, decisions, state changes, persistence boundaries, and meaningful failure paths. Use one overview diagram and focused subflows for behavior-changing branches, validation boundaries, asynchronous operations, retries, timeouts, or state transitions.

Diagram vocabulary:

- Rounded rectangle: component or class.
- Cylinder: persistent storage.
- Diamond: decision or validation.
- Solid arrow: synchronous call.
- Dashed arrow: asynchronous message, event, callback, or broadcast.
- Red path: rejection or failure.
- Blue boundary: external API or network boundary.
- Purple marker: observability.

Every diagram should include its flow name, Besu version, scope, legend, and an omitted-detail note.

Existing logs and tests may be used. Temporary local instrumentation is allowed when needed, but no instrumentation changes are to be committed to Besu. Do not record private keys, credentials, or unnecessary sensitive payload data.
