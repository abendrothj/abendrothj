# Jake Abendroth
**CS Undergrad @ University of San Francisco · Graduating December 2026**

I build things — mostly systems tooling and infrastructure in Rust and C, though I've shipped across the stack from AI pipelines to mobile apps. Co-founding a fintech startup on the side.

### 🏗️ Projects

* **`uutils/coreutils` (Open Source Contributor)**  
  Identified and mitigated a class of TOCTOU symlink race conditions across `install`, `ln`, and `tac`. Extended `safe_traversal.rs` to all Unix platforms and added fd-anchored primitives (`mkdir_at`, `open_file_at`, `create_dir_all_safe`, `copy_file_safe`) that became the foundation for subsequent fixes in the codebase. ([#9792](https://github.com/uutils/coreutils/pull/9792), [#10140](https://github.com/uutils/coreutils/pull/10140), [#10991](https://github.com/uutils/coreutils/pull/10991), [#11505](https://github.com/uutils/coreutils/pull/11505))

* **[`wisp`](https://github.com/abendrothj/wisp)**  
  Tailscale-native, agentless Docker operations dashboard built in Rust. Concurrent architecture with snapshot broadcasting and action channels. Dual TUI and local web interface with websocket live updates, Azure DB telemetry, and cross-platform releases.

* **[`LAO (Local AI Orchestrator)`](https://github.com/abendrothj/LAO)**  
  Offline-first AI workflow orchestrator in Rust. Custom DAG scheduler with level-based parallel execution and a dynamic plugin architecture that loads compiled `.dylib`/`.so` inference engines at runtime via FFI. Includes a native egui GUI with visual workflow editing.

* **[`Argus`](https://github.com/abendrothj/Argus)**  
  High-performance file integrity monitor in Rust. Parallel SHA-256 hashing with configurable thread count, recursive directory scanning, real-time monitoring, and NDJSON output for change tracking across large directory trees.

* **[`Finlingo`](https://finlingo.ai)** — Co-Founder & CTO  
  AI personal finance app for students and young professionals. Finny, the AI agent, monitors spending drift, surfaces subscription leaks, and answers natural language queries against your financial data. React Native frontend, domain-driven TypeScript backend, Plaid integration, and a two-step AI pipeline for intent classification and contextual response generation.

### ⚙️ Stack
**Languages:** Rust, C, Python  
**Systems:** Tokio, async concurrency, memory safety, FFI

### 📍 Currently
Finishing my CS degree while working on open source. Open to internships and new grad roles in systems, infrastructure, or security.

### 🔗
[jakea.net](https://jakea.net) · [LinkedIn](https://linkedin.com/in/jakeabendroth)
