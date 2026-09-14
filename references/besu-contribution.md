# Besu Contribution Guide for Zeeve

Guide on how to contribute to Besu.


## In what ways you can contribute to Besu?

- Code submissions
- Writing documentation
- raising issues
- helping others in chat
- any other actions that help develop Besu

## Requirement

- Github account with username ending with `<username>-zeeve`.
  - Please use zeeve mail to create this account
  - [GitHub account](https://github.com)
- Please create a personal Discord account
  - Most messages are exchanged over discord and will be easier to know and get confirmation about how you can contribute.
  - [Discord](https://discord.com/invite/hyperledger)
  - Check out the **#besu** channel
- [Besu setup for development and testing](#besu-setup-for-development)

## Besu setup for development

- First **setup a github** with **Zeeve** mail id
- Create a [**Fork the repository**](https://github.com/besu-eth/besu/fork)
- Clone the fork to your computer
  - `git clone -b main --single-branch --recurse-submodules git@github.com:<<username>>-zeeve/besu.git`
  - It is around *"4.3GB"* of download with recursive flag
- **Create topic branch**
  - Naming start as issue number if you are plaining for code change.
  - Example like : `fix/12321-bug-fix`
  - Always sign off your commits; check the [DCO section](https://github.com/besu-eth/besu/blob/main/CONTRIBUTING.md#developer-certificate-of-origin-dco).
- Before Creating a PR please ensure to test your changes.
  - `./gradlew clean check test`
- **Create a PR**
  - [pull request template](https://github.com/besu-eth/besu/blob/main/.github/pull_request_template.md)
  - If the PR addresses an existing issue, link it in the PR description using GitHub keywords such as `fixes #1234` or `refs #1234`.
  - **Add labels** to identify the type of your PR.
  - **Ensure your changes are reviewed**. Let us know on Discord that your PR is ready for review. If you are a maintainer, you can choose reviewers; otherwise this is done by one of the maintainers.
  - **When your PR is approved and validated**, all tests pass, and your branch has no conflicts, it can be merged. This is done by a maintainer, usually the same person who approves also merges it.
  - Besu maintains a [`CHANGELOG.md`](CHANGELOG.md) so users can see what changed between releases. Add your entry under the `## Unreleased` section


## Agentic contributions

- Yes, Agentic contributions are required and have a pattern.
- [Guidelines for submitting agentic contributions](https://github.com/besu-eth/besu/blob/main/CONTRIBUTING.md#guidelines-for-submitting-agentic-contributions)
- gist of it is to create `Co-Authored-By` or `Assited-By` keys in DCO statements, and include model name, and context size
Example

```text
Co-Authored-By: Codex gpt-5.6-luna (1M context) <noreply@anthropic.com>
Signed-off-by: Full Legal Name <fistname.lastname@zeeve.io>
```


