# Startup and Bootstrap

```text
Besu.main → BesuCommand.initialProcess → configure → buildController → buildRunner → startExternalServices → startEthereumMainLoop → NetworkRunner.start → Synchronizer.start
```

Important classes: `Besu`, `BesuCommand`, `BesuController`, `BesuControllerBuilder`, `Runner`, `RunnerBuilder`, `NetworkRunner`.

Use Dager and Pico cli to create commands and provide context to them.

These command are defined in the `BesuComponent` which is used as generated class `DagerBesuComponent`.

## Mental Model

- Pico CLI command runner:

  - When root command is run, i.e. `BesuCommand` then the run method is called that is responsible for starting the nodes
  - If root command is not called then sub commands are run.

- `BesuCommand` is the root command responsible for handling besu node startup.
- `BesuController` is a wrapper for all the required states, objects and interfaces that besu will require during its running lifetime. Mostly related to configuration and state of besu.
- `Runner` controls besu services lifecycle. Mostly related to the API and its related services.

- banned node ids are set in `BesuCommand.synchronyze()` to runner.


