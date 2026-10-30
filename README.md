# Marketplace

Local agent plugins published by Henrique K. The catalogs pin released plugin versions so installation is reproducible.

| Plugin | Version | Purpose |
| --- | --- | --- |
| [Harness](https://github.com/cekrauseee/harness) | 0.0.3 | Local context, memory, and explicit agent workflows. |

## Codex and local ChatGPT desktop

```sh
codex plugin marketplace add cekrauseee/marketplace
codex plugin add harness@marketplace
```

Start a new session. In ChatGPT desktop, restart if needed, open Plugins, and select Harness from `marketplace`. Use the setup skill to prepare the host. Local hook trust remains controlled by the host. These commands configure a local Git-backed marketplace; they do not publish to the universal public directory or deploy local tools to cloud-orchestrated ChatGPT Work.

## Claude Code

```sh
claude plugin marketplace add cekrauseee/marketplace
claude plugin install harness@marketplace
```

Start a new session and use `/harness:setup`. See the [Harness installation guide](https://github.com/cekrauseee/harness/blob/main/docs/installation.md) for prerequisites and host configuration.

## Catalogs

- `.agents/plugins/marketplace.json` is the Codex and local ChatGPT catalog.
- `.claude-plugin/marketplace.json` is the Claude Code compatibility catalog.

To publish an update, release the plugin first, update both catalogs to the same release tag, and verify installation in an isolated host configuration. Keep plugin identifiers consistent between catalogs and manifests.
