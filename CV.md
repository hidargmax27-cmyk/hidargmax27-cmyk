# Tyra Zhang

[Email](mailto:hidargmax27@gmail.com) | [GitHub](https://github.com/hidargmax27-cmyk) | [Portfolio](https://github.com/hidargmax27-cmyk) | Research manuscripts under submission / under review | Hong Kong | Open to Remote

## Security Tooling / Formal Verification Research Engineer

AI-Assisted Verification | Web3 Security Tooling | Program Analysis | Smart Contract Invariant Triage

## Summary

Security tooling and formal verification researcher building AI-assisted systems for code analysis and smart contract security. Designed and implemented CogniBridge, a 2800+ file production system with six-chain parallel detection architecture (symbolic execution, concolic, multi-agent red team, 4D fuzzing, taint tracking, graph reasoning) and real-time Mempool defense — iterated through 6 major versions with 84 engineering-level solutions. Authored MNS-Verify, a neuro-symbolic verification framework achieving 0.8748 Macro-F1 on a 443-instance benchmark. Currently extending toward smart contract invariant discovery and counterexample-guided audit triage. Interested in Web3 security roles focused on automated analysis, invariant discovery, fuzzing, formal verification, and audit workflow tooling.

## Web3 Security Tooling

### CogniBridge — AI-Driven Smart Contract Deep Audit & Real-Time Defense System

Full-stack production system | 2800+ source files | 6 major versions (v3.0 → v3.6) | 84 engineering solutions  
[GitHub](https://github.com/hidargmax27-cmyk/cognibridge) | [Website](https://cognitivebridgeai.com/) | [Technical Whitepaper (v3.6)](https://github.com/hidargmax27-cmyk/cognibridge)

**Architecture & Core Engine:**
- Designed and implemented six-chain parallel detection architecture: symbolic execution (Z3/CVC5/Boolector solver portfolio), concolic hybrid execution, multi-agent game-theoretic red team, 4D temporal fuzzing, EVM dynamic taint tracking, and FalkorDB knowledge graph reasoning.
- Built a solver portfolio strategy with XGBoost-predicted skip decisions and safety-critical exemption mechanisms, reducing NP-Hard constraint timeout rates by 70%+ on complex DeFi protocols.
- Implemented CodeBERT semantic vector pre-filtering combined with System Dependency Graph (SDG) dual-channel search, reducing cross-contract interaction search space by 85%+.

**Real-Time Defense (CogniBridge Shield):**
- Engineered three-layer deep interception: Mempool pre-execution simulation (<100μs/tx), Builder API integration for block-level filtering, and post-block verification with automatic rescue transaction injection.
- Designed multi-Builder parallel distribution with on-chain circuit breakers and rescue obfuscation engine for sandwich attack and frontrunning prevention.

**Formal Verification Pipeline:**
- Implemented property mutation testing as a deterministic safety net for LLM-generated CVL specifications — mutations that survive indicate weak or over-permissive properties, achieving 60%+ mutation kill rate threshold before verification proceeds.
- Built CVL Actor-Critic reinforcement learning loop: Generator proposes invariants, Critic validates via symbolic execution, feedback refines specification quality iteratively.

**Cloud-Edge & Operational:**
- Designed cloud-edge elastic scheduling with optimistic execution and conflict detection for 8GB-constrained edge nodes, enabling offline audit capability with incremental sync.
- Implemented TWAP time-window retrospective analysis with volatility anomaly detection and external anchor points for oracle manipulation detection.
- Built VS Code extension, Docker self-hosted deployment, and CI/CD integration (GitHub Actions / GitLab CI) for automated PR-level audit.

**Honest Capability Boundaries:**
- Documented 12 uncertainty marker types distinguishing verified findings from hypotheses; published detection rate matrices with explicit limitations (known patterns >94%, time-dimension attacks 62-82%, novel zero-days ~35%).

**Tech Stack:** Rust core + Tree-sitter AST + FalkorDB + React/tRPC + Foundry + CodeBERT + Z3/CVC5 + Stripe billing + Tauri desktop

---

### Vulnerability PoC Library

Foundry-based reproduction of real-world smart contract exploits  
[GitHub](https://github.com/hidargmax27-cmyk/vulnerability-foundry-poc)

- Built a library of Foundry-based proof-of-concept reproductions for documented smart contract vulnerabilities with detailed writeups.
- Covers reentrancy, oracle manipulation, access control bypass, flash loan attacks, and upgrade-related exploits.

---

## Selected Research

### Smart Contract Upgrade Safety Research

Manuscript under submission / under review  
Paper / preprint coming soon | Code / artifact coming soon

- Authored a research manuscript on semantic drift in smart contract upgrades: deviations where a new implementation violates the original business logic or security assumptions.
- Designed a neuro-symbolic pipeline combining AST-based symbolic diffing, LLM-assisted intent inference, and hybrid counterexample synthesis.
- Used Halmos symbolic execution and targeted Foundry fuzzing to validate LLM-generated invariants and synthesize concrete counterexamples.
- Built and evaluated on a real-world benchmark of upgradeable smart contract pairs covering proxy patterns, validation-logic regressions, access-control changes, and DeFi protocol evolution.
- Generated concrete counterexamples for upgrade-related semantic drift cases that static analyzers (Slither, Semgrep) fail to catch.

### MNS-Verify — Neuro-Symbolic Verification Framework

Manuscript under submission / under review  
[GitHub](https://github.com/hidargmax27-cmyk/MNS-Verify) | Paper / preprint coming soon

- Authored a research manuscript on neuro-symbolic verification for C++-to-Rust semantic equivalence checking.
- Designed a verification pipeline using LLM-guided specification extraction, property decomposition, SMACK, Z3, and bounded model checking.
- Built MultiSpec-Equiv, a benchmark of 443 C++-to-Rust migration instances, including 200 CVE-derived cases with ground-truth semantic labels.
- Achieved 0.8748 Macro-F1 against LLM-agent, symbolic execution, and static-analysis baselines — outperforming GPT-4 direct verification (0.71) and pure symbolic approaches (0.63).
- Developed a property-decomposed verification approach that decomposes semantic equivalence into independently checkable assertions, enabling parallel verification and granular failure localization.
- Currently extending the approach toward smart contract invariant discovery and counterexample-guided audit triage.

### MNS-Verify Contracts — AI-Assisted Smart Contract Invariant Triage

In progress  
Solidity / Foundry / Slither / Echidna / LLM Agents  
Code / demo coming soon

- Building an AI-assisted audit triage tool that extracts candidate invariants from Solidity projects and validates them with Foundry invariant tests, Slither signals, and fuzzing traces.
- Focuses on executable evidence: each high-confidence finding includes a failing test, fuzzing trace, SMT witness, or exploit reproduction — not unverified LLM claims.
- Targets security properties including accounting invariants, access control, reentrancy-state consistency, oracle assumptions, lifecycle constraints, and upgradeability risks.
- Designed the workflow around counterexample-guided refinement: invalid or weak invariants are repaired or discarded based on verifier and fuzzer feedback loops.

---

## Hackathon & Competition Projects

### AgentVault-0G — Self-Custodial AI Agent Billing Console

0G Hackathon Project  
[GitHub](https://github.com/hidargmax27-cmyk/agentvault-0g)

- Built a self-custodial AI agent billing console with 0G Storage memory and 0G Chain audit proofs.
- Implemented on-chain payment verification and decentralized storage for agent execution traces.

### CircuitSage — Rapid Security Agent

[GitHub](https://github.com/hidargmax27-cmyk/circuitsage-rapid-agent)

- Developed a rapid security analysis agent for smart contract circuits.

---

## Technical Skills

**Languages:** Python, TypeScript/Node.js, Solidity, Rust, C/C++

**Verification & Program Analysis:** Z3, CVC5, Boolector, SMT solving, bounded model checking, symbolic execution (Halmos, SMACK), property decomposition, invariant synthesis, concolic execution, fuzzing (Echidna, Foundry fuzz)

**Web3 Security:** Foundry, Slither, Semgrep, Echidna, EVM internals, DeFi protocol analysis, flash loan / MEV / oracle manipulation patterns, proxy upgrade safety, invariant testing, PoC reproduction

**AI/ML for Security:** LLM agents (OpenAI/Anthropic/DeepSeek), CodeBERT embeddings, RAG pipelines, tool calling, structured outputs, reinforcement learning for specification synthesis, XGBoost for constraint prioritization

**Systems & Infrastructure:** Rust, Tree-sitter, FalkorDB (graph DB), Docker, GitHub Actions, CI/CD pipelines, tRPC/React full-stack, Tauri desktop, Stripe integration, cloud-edge architecture

---

## Education / Independent Study

**The Hong Kong Polytechnic University**  
Coursework in Data Analytics, one year

**Independent Researcher**  
Self-directed study in formal verification, program analysis, smart contract security, AI systems, and Web3 developer tooling. Active contributor to open-source security tooling ecosystem.
