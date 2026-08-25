# Documentation TODO

Baseline: Besu `26.7.0` release tag.

Legend: `[ ]` not started · `[-]` in progress · `[x]` complete · `[?]` needs investigation.

## Repository setup

- [x] Create separate `besu-flow-documentation` repository.
- [x] Record the source baseline.
- [x] Define Markdown and draw.io conventions.
- [x] Define the first flow backlog.
- [ ] Decide whether and where to publish the repository.
- [ ] Decide whether to mirror finished documents into Google Docs/Drive.

## Core flow backlog

- [ ] System overview and flow map.
- [ ] Startup and bootstrap.
- [ ] Genesis and consensus-mode selection.
- [ ] JSON-RPC request lifecycle.
- [ ] Engine API `forkchoiceUpdated`.
- [ ] Engine API payload building and `getPayload`.
- [ ] Engine API `newPayload` validation.
- [ ] Transaction admission from JSON-RPC.
- [ ] Transaction admission from P2P.
- [ ] Transaction-pool replacement, eviction, and revalidation.
- [ ] Transaction selection for block creation.
- [ ] Block execution and state mutation.
- [ ] Proposed/received block validation.
- [ ] Canonical block import and world-state persistence.
- [ ] BFT block production: proposal, prepare, commit, quorum.
- [ ] BFT timeout, round-change, and invalid-proposal branches.
- [ ] PoS/Merge payload production.
- [ ] P2P startup and discovery.
- [ ] Inbound peer acceptance and rejection.
- [ ] ETH status exchange and peer activation.
- [ ] Block propagation.
- [ ] Transaction propagation.
- [ ] P2P message limits and constraints.

## Secondary flows

- [ ] Full synchronization.
- [ ] Snap synchronization.
- [ ] Reorganization and recovery.
- [ ] World-state storage variants and trie commits.
- [ ] Permissioning.
- [ ] Plugin lifecycle.
- [ ] Shutdown and restart.
- [ ] Metrics, logs, and tracing.

## Per-flow checklist

- [ ] Scope and trigger are stated.
- [ ] Important classes and functions are identified.
- [ ] Normal path is explained.
- [ ] Important failures, retries, and timeouts are explained.
- [ ] Shared and mode-specific behavior is separated.
- [ ] Overview and necessary subflow diagrams exist.
- [ ] Diagram and Markdown agree.
- [ ] Source references target Besu 26.7.0.
- [ ] Related flows are linked.
