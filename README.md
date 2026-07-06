# Jake Abendroth

**Systems & Infrastructure Engineer**

San Francisco, CA · Graduating December 2026 (BS Computer Science, USF)

I build high-performance systems tooling and isolated backend infrastructure, primarily in **Rust** and **C**. My work spans OS-level security mitigations (POSIX/kernel space), low-level memory management, and real-time AI agent architectures.

### 🏗️ Selected Work

* [**`simgit`**](https://github.com/abendrothj/simgit) — *Disk-Efficient Multi-Agent Git Worktrees (Rust)*
  Engineered a copy-on-write Git worktree CLI (`sg`) designed for concurrent AI agent isolation. Bypasses standard checkouts by leveraging APFS `clonefile`, Linux reflink, and `fuse-overlayfs` fallbacks to share a single baseline's physical disk blocks across N agents. Benchmarked at **8.0x less physical disk usage** for 8 concurrent agents compared to standard worktrees.

* **`uutils/coreutils`** — *Security Engineer & Core Contributor (Rust)*
  Patched critical TOCTOU (Time-of-Check to Time-of-Use) symlink race conditions across `install`, `ln`, and `tac` during the private-disclosure window of a Canonical-funded Zellic audit. Authored cross-platform mitigations extending fd-anchored primitives (`openat`, `mkdirat`) to bypass dynamic path resolution vulnerabilities.
  *Fixes cited for **CVE-2026-35356** and **CVE-2026-35362**, currently shipping in Ubuntu 26.04.* ([#9792](https://github.com/uutils/coreutils/pull/9792), [#10140](https://github.com/uutils/coreutils/pull/10140), [#10991](https://github.com/uutils/coreutils/pull/10991), [#11505](https://github.com/uutils/coreutils/pull/11505))

* [**`Finlingo`**](https://finlingo.ai) — *Co-Founder & CTO*
  Architected the backend infrastructure for an autonomous financial action-agent. Built a highly concurrent WebRTC voice pipeline (LiveKit) with custom SIP trunk telephony and VAD-based interruption handling. Secured user infrastructure using AES-256-GCM field-level encryption and isolated backend execution environments (LXC).

* [**`LAO`**](https://github.com/abendrothj/LAO) — *Local AI Orchestrator (Rust)*
  Offline-first AI workflow engine. Engineered a custom DAG scheduler that utilizes topological sorting and true OS threads for per-level parallel execution. Implemented a dynamic FFI plugin architecture (`libloading`) to load compiled `.dylib`/`.so` inference engines at runtime via a versioned C ABI.

* [**`wisp`**](https://github.com/abendrothj/wisp) — *Tailscale-Native Docker Dashboard (Rust)*
  Zero-trust, agentless infrastructure dashboard. Uses a concurrent architecture with snapshot broadcasting, a dual TUI/Web UI with WebSocket live updates, and secure Tailscale SSH tunneling.

### 📍 Currently

Pushing the limits of concurrent agent infrastructure and sprinting toward Q3 goals at Finlingo. Actively exploring **Systems, Core Infra, and Security Engineering roles** for Q1 2027.

### 🔗 Let's Connect

[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth) · contact@jakea.net
