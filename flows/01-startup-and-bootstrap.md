# Startup and Bootstrap

Flow ID: BESU-STARTUP-001  
Status: planned  
Baseline: Besu 26.7.0

Primary path:

```text
Besu.main → BesuCommand.initialProcess → configure → buildController → buildRunner → startExternalServices → startEthereumMainLoop → NetworkRunner.start → Synchronizer.start
```

Important classes: `Besu`, `BesuCommand`, `BesuController`, `BesuControllerBuilder`, `Runner`, `RunnerBuilder`, `NetworkRunner`.

```mermaid
```
