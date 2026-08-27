# Besu Flow Documentation

Developer-oriented documentation and diagrams for Hyperledger Besu 26.7.0.

This repository is separate from the official Besu source repository. Besu remains the implementation source of truth; this repository explains important runtime flows and links to the pinned source.

> [!NOTE]
> If the diagrams feel cluttered or not easy to read you can create a svg for it using the command.
> To Install mmdc run `npm install -g @mermaid-js/mermaid-cli`
> and run for the diagram `mmdc -i <diagram.mmd> -o <diagram.svg> -p puppeteer-config.json`

## Working conventions

- Markdown files are the authoritative narrative.
- Native `.mmd` files are the authoritative diagrams.
- The documented baseline is the `26.7.0` release tag.
- Google Docs/Drive copies are optional publishing artifacts.
- Focused diagrams link to detailed subflows instead of attempting one repository-wide diagram.

Start with [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Flow documents

- [Startup and bootstrap](flows/01-startup-and-bootstrap.md)
<!-- - [JSON-RPC and Engine API](flows/02-json-rpc-and-engine-api.md) -->
<!-- - [Transaction lifecycle](flows/03-transaction-lifecycle.md) -->
<!-- - [Block execution and import](flows/04-block-execution-and-import.md) -->
<!-- - [Block production and consensus](flows/05-block-production-and-consensus.md) -->
<!-- - [P2P networking](flows/06-p2p-networking.md) -->
<!-- - [Synchronization](flows/07-synchronization.md) -->
<!-- - [World state and storage](flows/08-world-state-and-storage.md) -->
<!-- - [Permissioning and plugins](flows/09-permissioning-and-plugins.md) -->
<!-- - [Observability and failures](flows/10-observability-and-failures.md) -->
