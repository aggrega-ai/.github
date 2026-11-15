<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="mark-dark.svg">
    <img src="mark-primary.svg" alt="Aggrega" width="140">
  </picture>
</p>

<h1 align="center">Aggrega</h1>

<p align="center">
  <strong>Describe the architecture once. Get the infrastructure code for each platform you run.</strong>
</p>

<p align="center">
  <a href="https://aggrega.ai">Website</a> ·
  <a href="https://aggrega.ai/docs/getting-started/">Getting started</a> ·
  <a href="https://aggrega.ai/docs/">Documentation</a> ·
  <a href="https://aggrega.ai/docs/language-reference/examples/">Examples</a> ·
  <a href="https://aggrega.ai/catalog/browse">Catalog</a>
</p>

Aggrega is an open-source compiler for infrastructure as code: one YAML description of your application becomes
Kubernetes, Helm, Compose, Terraform or CloudFormation files you review and own.

Already built an agent with LangGraph, CrewAI, n8n, Dify and more? `aggrega import` reads it and writes draft Aggrega
files for you to review and edit.

## How it works

You describe the application, Aggrega writes the files, and the tools you already use deploy them. Aggrega never
reaches a running cluster or a cloud account.

- An **Aggregate** names its components and how they connect.
- A **Release** fills in one environment's settings.
- A **Manifest** maps each component to a Recipe for your platform, such as a Helm chart, a Terraform module or a
  container.
- `aggrega build` writes the files for each platform: the same files for the same input, every time, with every
  dependency pinned in a lockfile.
- ArgoCD, Flux or Terraform deploys what it wrote.

Your policies plug into the compiler and stop a build that breaks them, saying what to fix. A policy never changes
your files to make them pass.

## Install

```sh
curl -fsSL https://aggrega.ai/install.sh | sh
```

```powershell
irm https://aggrega.ai/install.ps1 | iex
```

One command installs the `aggrega` binary for your user, with no administrator rights. It also works with your AI
assistant: `aggrega mcp` gives an assistant Aggrega's tools — scaffold, validate, build and the rest. See
[setting up an AI assistant](https://aggrega.ai/docs/ai-assistants/set-up/).

## Repositories

| Repository | What it holds |
|---|---|
| [aggrega-cli](https://github.com/aggrega-ai/aggrega-cli) | The compiler and the `aggrega` command-line interface |
| [aggrega-vscode-extension](https://github.com/aggrega-ai/aggrega-vscode-extension) | Validation, navigation, hover and completion for Aggrega YAML in Visual Studio Code |
| [aggrega-docs](https://github.com/aggrega-ai/aggrega-docs) | The documentation published at aggrega.ai/docs |
| [aggrega-hub](https://github.com/aggrega-ai/aggrega-hub) | The standard-library catalog of Components, Features, Recipes and plugins |
| [aggrega-schemas](https://github.com/aggrega-ai/aggrega-schemas) | The JSON Schemas of every Aggrega entity |
| [aggrega-pdk](https://github.com/aggrega-ai/aggrega-pdk) | Plugin development kits for Go, Rust and TypeScript |
| [aggrega-abi](https://github.com/aggrega-ai/aggrega-abi) | The codecs of the plugin ABI, in Go, Rust and TypeScript |
| [aggrega-plugins](https://github.com/aggrega-ai/aggrega-plugins) | Plugins built with the kits and published to the hub |
| [aggrega-skills](https://github.com/aggrega-ai/aggrega-skills) | The skill that teaches an AI assistant to install and use Aggrega |

## Open source

The Aggrega compiler is open source under Apache-2.0, and stays that way: there will be no closed edition of the
compiler, no open-core. All the features of the compiler will be available in the open source version.
