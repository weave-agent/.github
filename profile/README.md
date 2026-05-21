# Weave

Weave is a lightweight, extensible coding agent framework written in Go.

The core framework provides an event-driven SDK, dynamic extension loading, provider-neutral model support, and a terminal-first developer experience. Extensions own individual capabilities and communicate through bus events, so tools, providers, UIs, storage, and agent behavior can evolve independently.

## Core repositories

- [weave](https://github.com/weave-agent/weave) — core framework, SDK, launcher, settings, and event bus
- [weave-tui](https://github.com/weave-agent/weave-tui) — terminal UI extension
- [homebrew-tap](https://github.com/weave-agent/homebrew-tap) — Homebrew installation tap

## Public extensions

### Providers

- [weave-anthropic](https://github.com/weave-agent/weave-anthropic)
- [weave-openai](https://github.com/weave-agent/weave-openai)
- [weave-zai](https://github.com/weave-agent/weave-zai)

### Tools

- [weave-bash](https://github.com/weave-agent/weave-bash)
- [weave-edit](https://github.com/weave-agent/weave-edit)
- [weave-find](https://github.com/weave-agent/weave-find)
- [weave-grep](https://github.com/weave-agent/weave-grep)
- [weave-ls](https://github.com/weave-agent/weave-ls)
- [weave-read](https://github.com/weave-agent/weave-read)
- [weave-webfetch](https://github.com/weave-agent/weave-webfetch)
- [weave-write](https://github.com/weave-agent/weave-write)

## Install

```bash
brew install weave-agent/tap/weave
```

## Development

```bash
git clone https://github.com/weave-agent/weave.git
cd weave
make test
make lint
```

Extensions are independent Go modules. Each extension owns one concern and integrates with the framework through the SDK and event bus.
