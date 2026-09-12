# Jake Abendroth

**Systems & Security Engineer**

San Jose, CA · Graduating December 2026 (BS Computer Science, USF) · Available January 2027

I build systems software in **Rust** — filesystem security, POSIX correctness, and low-level tooling. Most of my public work is upstream in projects other people depend on.

## At a glance

- **Security:** upstream fixes for filesystem TOCTOU races, parser stack overflows, and Git staging corruption.
- **Systems:** Rust tooling focused on filesystem behavior, POSIX correctness, and low-level reliability.
- **Local AI:** building offline workflow orchestration and capability-aware inference routing.

## Selected work

### [`uutils/coreutils`](https://github.com/uutils/coreutils) — Contributor (Rust)

- Patched TOCTOU symlink races in `install`, `ln`, and `tac` with fd-anchored traversal primitives in `uucore`.
- Extended the security coverage from Linux to macOS and FreeBSD; rewrote `expr`'s recursive-descent parser iteratively to prevent stack overflows.
- Official remediation for [CVE-2026-35356](https://github.com/uutils/coreutils/pull/10140); cited fix for [CVE-2026-35362](https://github.com/uutils/coreutils/pull/10991). Both ship in Ubuntu 26.04.
- Related work: [#9792](https://github.com/uutils/coreutils/pull/9792) · [#11505](https://github.com/uutils/coreutils/pull/11505) · [#13333](https://github.com/uutils/coreutils/pull/13333)

### [`zed-industries/zed`](https://github.com/zed-industries/zed) — Contributor (Rust)

Fixed Git staging corruption caused by ambiguous diff-hunk placement between the text buffer and diff engine. [#60584](https://github.com/zed-industries/zed/pull/60584) · resolves [#60424](https://github.com/zed-industries/zed/issues/60424)

### [`simgit`](https://github.com/abendrothj/simgit) — Copy-on-Write Git Worktrees (Rust)

Rust CLI (`sg`, published as [`simgit-cli`](https://crates.io/crates/simgit-cli)) for real Git linked worktrees backed by APFS `clonefile`, Linux reflinks, and unprivileged `fuse-overlayfs`.

On `microsoft/vscode` (18,707 tracked paths), each extra worktree costs **9.8–10.8 MiB against 567 MiB** for plain `git worktree` — about 0.4 KiB per tracked path plus ~60 KiB fixed. Cold setup for eight worktrees runs 6.4 s against 14.0 s.

### [`LAO`](https://github.com/abendrothj/lao) — Local AI Workflow Orchestrator (Rust)

Versioned C-ABI plugins load at runtime; YAML workflows compile to validated DAGs and execute in parallel by dependency level. FFI layout assertions, panic containment, and fuzzing protect the plugin boundary.

### [`pig`](https://github.com/abendrothj/pig) — Capability-Aware Inference Gateway (Rust)

Routes requests across heterogeneous local backends using measurable model, hardware, and runtime capabilities. Exposes an OpenAI-compatible chat-completions API while keeping scheduling separate from agent planning.

### Finlingo — Co-Founder & CTO (2026)

Built Plaid ingestion and normalization, a two-stage extraction/generation pipeline, field-level AES-256-GCM protection for access tokens and PII, and HMAC-verified webhook ingestion.

## Currently

Looking for **systems, infrastructure, and security engineering** roles starting January 2027. Bay Area or remote.

## Contact

[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth) · contact@jakea.net
