# Startup and Bootstrap

Flow ID: BESU-STARTUP-001  
Status: planned  
Baseline: Besu 26.7.0

Primary path:

```text
Besu.main → BesuCommand.initialProcess → configure → buildController → buildRunner → startExternalServices → startEthereumMainLoop → NetworkRunner.start → Synchronizer.start
```

Important classes: `Besu`, `BesuCommand`, `BesuController`, `BesuControllerBuilder`, `Runner`, `RunnerBuilder`, `NetworkRunner`.

- Pico CLI command runner:

  - When root command is run, i.e. `BesuCommand` then the run method is called that is responsible for starting the nodes
  - If root command is not called then sub commands are run.

- s
