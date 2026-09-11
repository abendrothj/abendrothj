# Jake Abendroth

**Systems & Security Engineer**

San Jose, CA · Graduating December 2026 (BS Computer Science, USF) · Available January 2027

I build systems software in **Rust** — filesystem security, POSIX correctness, and low-level tooling. Most of my public work is upstream in projects other people depend on.

### Selected Work

- [**`uutils/coreutils`**](https://github.com/uutils/coreutils) — *Contributor (Rust)*

  Patched TOCTOU symlink race conditions in `install`, `ln`, and `tac` during a Canonical-funded Zellic security audit. The durable fix was structural: fd-anchored traversal primitives (`mkdir_at`, `open_file_at`, `copy_file_safe`) in `uucore`'s `safe_traversal`, which walk a path component by component holding a directory descriptor rather than resolving the path twice and hoping it didn't change in between. Extended that coverage from Linux to macOS and FreeBSD. Separately, rewrote `expr`'s recursive-descent parser as an iterative one, eliminating stack overflows on deeply nested input.

  *Official remediation for* ***CVE-2026-35356***; *cited fix for* ***CVE-2026-35362***. *Both shipping in Ubuntu 26.04.*
  [#10140](https://github.com/uutils/coreutils/pull/10140) · [#10991](https://github.com/uutils/coreutils/pull/10991) · [#9792](https://github.com/uutils/coreutils/pull/9792) · [#11505](https://github.com/uutils/coreutils/pull/11505) · [#13333](https://github.com/uutils/coreutils/pull/13333)

- [**`zed-industries/zed`**](https://github.com/zed-industries/zed) — *Contributor (Rust)*

  Fixed Git staging corruption caused by ambiguous diff-hunk placement between the text buffer and the diffing engine, keeping invalid hunk evaluations from reaching the UI.
  [#60584](https://github.com/zed-industries/zed/pull/60584) · resolves [#60424](https://github.com/zed-industries/zed/issues/60424)

- [**`simgit`**](https://github.com/abendrothj/simgit) — *Copy-on-Write Git Worktrees (Rust)*

  A Rust CLI (`sg`, published as [`simgit-cli`](https://crates.io/crates/simgit-cli)) that provisions real Git linked worktrees from a shared immutable baseline via APFS `clonefile` and Linux reflinks, with an unprivileged `fuse-overlayfs` backend for ext4 and CI, and a `--require-cow` guard that fails loudly instead of silently falling back to a full copy.

  On `microsoft/vscode` (18,707 tracked paths), each additional worktree costs **9.8–10.8 MiB against 567 MiB** for plain `git worktree` — about 0.4 KiB per tracked path plus ~60 KiB fixed. Content size doesn't enter into it: files from 4 KiB to 64 MiB cost the same per file, because `clonefile` shares the extent tree by reference rather than copying it. Cold setup for eight worktrees runs 6.4 s against 14.0 s.

  The repo reports marginal cost rather than a ratio on purpose — "8× less disk at 8 worktrees" is just the worktree count restated, and the same run yields 50× at fifty.

- [**`LAO`**](https://github.com/abendrothj/lao) — *Local AI Workflow Orchestrator (Rust)*

  A plugin system built on a versioned C ABI (v2, minimum supported v1), loading `.so`/`.dylib`/`.dll` at runtime via `dlopen`. v2 vtable fields append after a frozen v1 prefix so existing plugins keep loading; offset assertions and an FFI fuzz suite guard the layout. Plugin panics are contained at every `extern "C"` boundary — an unwind across it aborts the host — and mapped to structured error statuses. YAML workflows compile to a DAG validated for plugin availability and I/O type compatibility, then execute in parallel by dependency level.

- [**`pig`**](https://github.com/abendrothj/pig) — *Capability-Aware Inference Gateway (Rust)*

  Treats each model, hardware target, and runtime configuration as a schedulable `ModelInstance`, routing requests across heterogeneous backends on measurable capabilities and live runtime signals — vision support, reasoning modes, placement policy, context limits, availability. Exposes an OpenAI-compatible chat-completions API, with scheduling kept separate from agent planning.

- **Finlingo** — *Co-Founder & CTO* (2026)

  Backend for a personal finance product. Integrated Plaid for bank linking and transaction ingestion, normalizing institution data into a consistent internal schema, and built a two-stage LLM pipeline over it that separated extraction from generation. Protected access tokens and PII with field-level AES-256-GCM encryption and HMAC-verified webhook ingestion.

### Currently

Looking for **systems, infrastructure, and security engineering** roles starting January 2027. Bay Area or remote.

### Contact

[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth) · contact@jakea.net
