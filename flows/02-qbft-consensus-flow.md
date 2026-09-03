# Besu Flow Documentation for QBFT Consensus

- `QbftBesuControllerBuilder` is responsible for creation of QBFT controller.

- QBFT event handler do not implement the `BftEventHandler`. Rather it uses a `BftEventHandlerAdaptor` to convert the `QbftEventHandler` implementation `QbftController` to `BftEventHandler`.

- QbftV1
  - PROPOSAL = 0x12
  - PREPARE = 0x13
  - COMMIT = 0x14
  - ROUND_CHANGE = 0x15
  - MESSAGE_SPACE = 0x16

- all Message where round identifier is less than equal to chain head block number are ignored
  - Discard all messages which target the BLOCK-CHAIN height (which SHOULD be 1 less than the `currentHeightManager`, but CAN be the same directly following import).

- peers should not be used for accessing the network as it does not enforce the "only send once" filter applied by the `UniqueMessageMulticaster`.
  - They use `istanbul` protocol


## Flows TODO

- `QbftRound.java:374` `blockImporter.importBlock(...)`
- `NettyPeerConnection.java`
- `QbftRound.notifyNewBlockListeneres(...)`
- DB state
- Block production slows down, transaction pool

- `QbftBlockHeightManager.buildBlockAndMaybePropose()`
  - Only stay idle while the chain is genuinely quiet.
  - If a transaction has arrived after the block period but before the empty block period, the block this height would produce is now non-empty.
  - Usually the proposer would receive the transaction over P2P and break out of its empty block timer, but if the proposer crashes during the empty block period the chain is stalled until the full empty block period expires (possibly many minutes or hours).
