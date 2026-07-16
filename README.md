# CortexClaw

Self-contained personal AI agent platform that runs locally: a web dashboard,
an agent runtime gateway, and a pluggable tool system, with isolated per-agent
memory.

This repository distributes **prebuilt Linux x86-64 binaries**. There is no
source to build and no build step required — download, make executable, and run.

## What's in this release

| File                 | Purpose                                                                            |
|----------------------|------------------------------------------------------------------------------------|
| `cortexclaw`         | Gateway / agent runtime. Hosts the agent loop, tools, and channels (port 18790).   |
| `cortexclaw-launcher`| System-tray launcher with an embedded web dashboard (port 18800). Starts the gateway as a separate process and opens the dashboard. |

## Requirements

- Linux x86-64 (amd64)
- Optional: a Chromium-based browser on `PATH` for the browser-automation tool

## Run

```sh
chmod +x cortexclaw cortexclaw-launcher
./cortexclaw-launcher
```

The launcher opens the dashboard in your browser and starts the gateway as a
separate process. Bring your own API keys for the model providers you want to
use; configuration and per-agent memory are stored under `~/.cortexclaw/`.

## Version

v0.1.1 — first public release.