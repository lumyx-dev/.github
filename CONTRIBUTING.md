# Contributing to Lumyx

Lumyx is early. That means two things: the codebase is small enough to understand in an
afternoon, and the decisions that will matter in two years are being made right now. Both make
it a good moment to contribute.

This file holds the guidelines shared by every repository in the `lumyx-dev` organization. Each
repository's own `CONTRIBUTING.md` or `README.md` covers its setup — for the SFU, read
[sfu-core's CONTRIBUTING.md](https://github.com/lumyx-dev/sfu-core/blob/main/CONTRIBUTING.md)
before touching the media path.

---

## Where to start

| You want to… | Go to |
|---|---|
| Work on the media server | [`sfu-core`](https://github.com/lumyx-dev/sfu-core) — Rust |
| Improve the self-hosted dashboard | [`dashboard`](https://github.com/lumyx-dev/dashboard) — Next.js |
| Fix or add a design-system component | [`ui`](https://github.com/lumyx-dev/ui) — React + Tailwind |
| Fix the docs or the website | [`website`](https://github.com/lumyx-dev/website) — Next.js + Fumadocs |

Questions, "does it do X?" and setup trouble go to
[**Discussions**](https://github.com/lumyx-dev/sfu-core/discussions) rather than issues — answers
there stay searchable for whoever hits the same wall next.

---

## Licensing

By contributing you agree your work ships under the license of the repository you contribute
to: **AGPL-3.0-only** for `sfu-core` and `dashboard`, **MIT** for `ui` and `website`.

---

## Before you open a PR

Every repository runs the same checks in CI as you can run locally:

- **Rust** (`sfu-core`): `cargo fmt --check`, `cargo clippy --all-targets -- -D warnings`, `cargo test`
- **TypeScript** (the others): `bun install`, `bun run lint`, `bun run check-types`,
  `bun run build` — plus `bun test` and `bun run verify:ds` where they exist

Keep them green. Don't reach for `#[allow(dead_code)]` or `// eslint-disable` to silence
something; if a symbol is unused, either wire it up or say in a comment why it stays.

---

## Conventions

**Commits** use [Conventional Commits](https://www.conventionalcommits.org/):
`feat(media): ...`, `fix(engine): ...`, `docs: ...`, `refactor(peer): ...`.

**Keep PRs focused.** A media-path change and a dashboard refactor are two PRs — in two
repositories.

**Formatting** is whatever the tooling produces (`cargo fmt`, ESLint). Run it.

**Language.** Identifiers, types and public documentation are in English. Code comments and log
messages in the existing code are mostly in French — follow the surrounding file rather than
mixing.

**Design system.** UI code uses the `@lumyx/ui` tokens; `bun run verify:ds` rejects literal
colours outside the token file.

---

## Reporting bugs

The useful report says what you ran, what you expected and what happened instead. For anything
media-related, also include:

- number of peers and what each was publishing (audio, video, both)
- browser and version
- `SFU_LOG=debug` server output around the failure
- a `chrome://webrtc-internals` dump if you're on Chrome — it's usually more informative than the
  server logs

---

## Code of conduct

Everyone taking part in Lumyx spaces follows the [Code of Conduct](CODE_OF_CONDUCT.md).
