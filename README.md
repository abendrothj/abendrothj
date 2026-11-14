# Jake Abendroth

**Software engineer** · systems, infrastructure, security · Bay Area, CA
BS Computer Science, University of San Francisco, May 2027 · Available June 2027 · Open to remote or relocation

I build software that has to be correct: filesystem tools, developer tooling, backend services for sensitive data, and local AI infrastructure, mostly in Rust. Most of my public work is upstream, in tools other people depend on.

**30+ merged PRs to uutils/coreutils · fixes for 2 CVEs shipping in Ubuntu 26.04 · [`simgit-cli`](https://crates.io/crates/simgit-cli) on crates.io**

## Work

| Project | What it is | Highlights |
|---|---|---|
| [**uutils/coreutils**](https://github.com/uutils/coreutils/pulls?q=is%3Apr+author%3Aabendrothj+is%3Amerged) | Rust rewrite of GNU coreutils, shipped in Ubuntu | [![merged PRs](https://img.shields.io/github/issues-search?query=repo%3Auutils%2Fcoreutils%20is%3Apr%20is%3Amerged%20author%3Aabendrothj&label=merged%20PRs&color=2ea44f)](https://github.com/uutils/coreutils/pulls?q=is%3Apr+author%3Aabendrothj+is%3Amerged) Official fix for [CVE-2026-35356](https://github.com/uutils/coreutils/pull/10140), cited fix for [CVE-2026-35362](https://github.com/uutils/coreutils/pull/10991) |
| [**QuackXide**](https://github.com/Code-Pause-Inc/QuackXide) | Team project, in progress: a database for protected data where plaintext exists only inside attested enclaves | Attestation verification for Confidential Space on Intel TDX |
| [**simgit**](https://github.com/abendrothj/simgit) | Copy-on-write Git worktrees for running many agents on one repo | [![crates.io](https://img.shields.io/crates/v/simgit-cli?label=crates.io)](https://crates.io/crates/simgit-cli) 10 MiB per extra worktree vs 567 MiB for `git worktree` on `microsoft/vscode` |
| [**zed**](https://github.com/zed-industries/zed/pull/60584) | Code editor | Fixed Git staging corruption from ambiguous diff-hunk placement |

Also: [LAO](https://github.com/abendrothj/lao), a DAG workflow engine with runtime-loaded C-ABI plugins · [pig](https://github.com/abendrothj/pig), a capability-aware gateway for local llama.cpp and MLX workers

## Security work

**uutils/coreutils**

- Closed TOCTOU symlink races in `install`, `ln`, and `tac` with fd-anchored traversal primitives in `uucore`.
- Hardened recursive `cp`, `chmod`, and `chown` against symlinked targets and directories swapped mid-walk.
- Brought the safe traversal layer to macOS, FreeBSD, AIX, and GNU Hurd; fixed SELinux `-Z` context lookup for relative paths.
- Rewrote `expr`'s recursive-descent parser iteratively to remove stack overflows on deeply nested input.

**QuackXide** (in progress)

- Verify Confidential Space attestation tokens on Intel TDX, with bounded token age and fuzzed claim decoding.
- Wrote the design record for key custody and attested key release.
- Removed fail-open configuration defaults from the query engine.
- Locked down outbound connectors: HTTPS only, no redirects, capped response bodies.

## Currently

Finishing QuackXide this semester. Looking for **software engineering** roles starting June 2027: systems, backend, infrastructure, developer tools, or security. Bay Area or remote.

## Contact

[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth) · contact@jakea.net
