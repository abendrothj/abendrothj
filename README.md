# Jake Abendroth

**Systems & Infrastructure Engineer**

San Francisco, CA · Graduating December 2026 (BS Computer Science, USF)

I build high-performance systems tooling and isolated backend infrastructure, primarily in **Rust**. My work spans OS-level security mitigations (POSIX/kernel space), low-level memory management, and real-time AI agent architectures.

### 🏗️ Selected Work

- [**`uutils/coreutils`**](https://github.com/uutils/coreutils) — *Contributor (Rust)*

  Patched critical TOCTOU (Time-of-Check to Time-of-Use) symlink race conditions across `install`, `ln`, and `tac` during the private-disclosure window of a Canonical-funded Zellic audit. Authored cross-platform mitigations extending fd-anchored primitives (`openat`, `mkdirat`) to bypass dynamic path resolution vulnerabilities. Engineered an iterative parser for the `expr` utility, completely eliminating stack overflow faults for deeply nested inputs. ([#13333](https://github.com/uutils/coreutils/pull/13333))
  
  *Fixes cited for* ***CVE-2026-35356*** *and* ***CVE-2026-35362****, currently shipping in Ubuntu 26.04.* ([#9792](https://github.com/uutils/coreutils/pull/9792), [#10140](https://github.com/uutils/coreutils/pull/10140), [#10991](https://github.com/uutils/coreutils/pull/10991), [#11505](https://github.com/uutils/coreutils/pull/11505))

- [**`zed-industries/zed`**](https://github.com/zed-industries/zed) — *Contributor (Rust)*

  Resolved Git staging corruption in the user interface by patching the `buffer_diff` implementation. Addressed underlying synchronization issues between the text buffer and the diffing engine to prevent invalid hunk evaluations from propagating to the UI. ([#60584](https://github.com/zed-industries/zed/pull/60584), resolving [#60424](https://github.com/zed-industries/zed/issues/60424))

- [**`pig`**](https://github.com/abendrothj/pig) — *Private Inference Gateway (Rust)*

  Building a capability-aware inference gateway that treats each running model, hardware target, and runtime configuration as a schedulable `ModelInstance`. Implemented constraint-based routing across heterogeneous backends using measurable capabilities and live runtime signals, including vision support, reasoning modes, placement policy, context limits, and availability. Exposes an OpenAI-compatible chat-completions API while keeping inference scheduling and execution cleanly separated from higher-level agent planning.

- [**`simgit`**](https://github.com/abendrothj/simgit) — *Disk-Efficient Multi-Agent Git Worktrees (Rust)*

  Engineered a copy-on-write Git worktree CLI (`sg`) designed for concurrent AI agent isolation. Bypasses standard checkouts by leveraging APFS `clonefile`, Linux reflink, and `fuse-overlayfs` fallbacks to share a single baseline's physical disk blocks across N agents. Benchmarked at **8.0x less physical disk usage** for 8 concurrent agents compared to standard worktrees.

- [**`Finlingo`**](https://finlingo.ai) — *Co-Founder & Lead Engineer*

  Architected the backend infrastructure for an autonomous financial action-agent. Built a highly concurrent WebRTC voice pipeline (LiveKit) with custom SIP trunk telephony and VAD-based interruption handling. Secured user infrastructure using AES-256-GCM field-level encryption and isolated backend execution environments (LXC).

### 📍 Currently

Pushing the limits of local agent infrastructure and sprinting toward Q3 goals at Finlingo. Actively exploring **Systems, Core Infra, and Security Engineering roles** for Q1 2027.

### 🔗 Let's Connect

[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth) · contact@jakea.net
