# Important Classes

| Responsibility | Representative classes |
|---|---|
| Startup | `Besu`, `BesuCommand`, `Runner` |
| Controller construction | `BesuController`, `BesuControllerBuilder` |
| API | JSON-RPC method classes, `ExecutionEngineJsonRpcMethods` |
| Transactions | `TransactionPool`, `TransactionValidator`, `MainnetTransactionValidator` |
| Block creation | `MiningCoordinator`, `AbstractBlockCreator`, `BlockTransactionSelector` |
| Block validation/import | `MainnetBlockValidator`, `MainnetBlockImporter` |
| Execution/state | `MainnetTransactionProcessor`, `AbstractBlockProcessor`, `PathBasedWorldState` |
| P2P | `NetworkRunner`, `DefaultP2PNetwork`, `RlpxAgent`, `EthProtocolManager`, `EthPeers` |
| Consensus | `BftMiningCoordinator`, `IbftRound`, `QbftRound`, `MergeCoordinator` |
