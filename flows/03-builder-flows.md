## Important startup items still left

Your major startup path is covered, but these areas still need attention:

- BesuControllerBuilder
  - Where Synchronizer and MiningCoordinator are created.
  - Consensus-specific builder selection.
  - Blockchain, world state, transaction pool, protocol context, and peer services.

- RunnerBuilder
  - How HTTP, P2P, NAT, synchronizer, mining, and metrics services are assembled into Runner.

- P2P startup internals
  - NetworkRunner.start()
  - DefaultP2PNetwork.start()
  - RlpxAgent.start()
  - peer discovery startup.

- Shutdown flow
  - Runner.awaitStop()
  - shutdown hook
  - stopping synchronizer, mining coordinator, P2P, RPC, and storage-related services.

- Startup failure paths
  - invalid options,
  - port conflicts,
  - controller construction failures,
  - RPC startup failures,
  - P2P startup failures,
  - synchronizer failures.
