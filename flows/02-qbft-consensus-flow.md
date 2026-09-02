# Besu Flow Documentation for QBFT Consensus

- `QbftBesuControllerBuilder` is responsible for creation of QBFT controller.

- QBFT event handler do not implement the `BftEventHandler`. Rather it uses a `BftEventHandlerAdaptor` to convert the `QbftEventHandler` implementation `QbftController` to `BftEventHandler`.
