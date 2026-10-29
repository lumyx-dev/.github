<p align="center">
  <img alt="Lumyx" src="https://raw.githubusercontent.com/lumyx-dev/website/main/brand/lumyx-github-1280x640.png" width="100%">
</p>

# Lumyx

**An open-source WebRTC SFU in Rust, with observability built into the media path — not bolted on.**

When a call degrades, the SFU is the only process that actually knows why: jitter, loss, NACKs,
keyframe requests. Lumyx keeps that knowledge instead of throwing it away — the forwarding engine
and the metrics pipeline are the same codebase.

> **Alpha.** The media path works end to end; the quality-metrics milestone is next.
> [Project status](https://github.com/lumyx-dev/sfu-core#project-status).

## Repositories

| Repository | What it is | License |
|---|---|---|
| [**sfu-core**](https://github.com/lumyx-dev/sfu-core) | The SFU — Rust, on [str0m](https://github.com/algesten/str0m). Start here. | AGPL-3.0 |
| [**dashboard**](https://github.com/lumyx-dev/dashboard) | Self-hosted real-time dashboard (Next.js) | AGPL-3.0 |
| [**ui**](https://github.com/lumyx-dev/ui) | `@lumyx/ui`, the Lumyx design system (React + Tailwind CSS v4) | MIT |
| [**website**](https://github.com/lumyx-dev/website) | [lumyx.dev](https://lumyx.dev) and [docs.lumyx.dev](https://docs.lumyx.dev) | MIT |

Self-hosting Lumyx unmodified for your own product triggers no AGPL obligation —
[AGPL & you](https://github.com/lumyx-dev/sfu-core#agpl--you).

## Get involved

- **Questions and ideas:** [sfu-core Discussions](https://github.com/lumyx-dev/sfu-core/discussions)
- **Contributing:** [CONTRIBUTING.md](https://github.com/lumyx-dev/.github/blob/main/CONTRIBUTING.md)
- **Docs:** [docs.lumyx.dev](https://docs.lumyx.dev)
