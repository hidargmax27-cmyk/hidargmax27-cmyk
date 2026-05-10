# Tyra Zhang

Security tooling and formal verification researcher building AI-assisted systems for code analysis and Web3 security.

[GitHub](https://github.com/hidargmax27-cmyk) | [CV](./CV.md) | Paper: MNS-Verify manuscript under submission / under review | Demo: Coming soon | Hong Kong | Open to Remote

## Current Focus

- **MNS-Verify**: neuro-symbolic verification for C++-to-Rust semantic equivalence checking.
- **MNS-Verify Contracts**: AI-assisted smart contract invariant triage and counterexample-guided audit workflows.
- **Web3 Security Tooling**: automated analysis, invariant discovery, fuzzing, formal verification, and audit workflow automation.

## Selected Work

### MNS-Verify

Manuscript under submission / under review.

MNS-Verify is a neuro-symbolic verification framework for semantic equivalence checking. It combines LLM-guided specification extraction, property decomposition, SMT solving, and bounded model checking.

Key points:

- Designed a verification pipeline using LLM-guided specification extraction, SMACK, Z3, and bounded model checking.
- Built MultiSpec-Equiv, a benchmark of 443 C++-to-Rust migration instances, including 200 CVE-derived cases.
- Evaluated against LLM-agent, symbolic execution, and static-analysis baselines.
- Developed a property-decomposed verification approach that turns semantic equivalence into independently checkable assertions.

Links: Paper / preprint coming soon | Code / artifact coming soon

### MNS-Verify Contracts

In progress.

MNS-Verify Contracts extends the MNS-Verify direction toward smart contract security. The goal is to build an AI-assisted audit triage tool that extracts candidate invariants from Solidity projects and validates them with executable evidence.

Planned workflow:

- Extract candidate invariants from Solidity contracts, tests, comments, and protocol documentation.
- Validate invariants with Foundry invariant tests, Slither signals, Echidna fuzzing traces, and symbolic reasoning where applicable.
- Produce counterexample traces, failing tests, and Markdown audit findings instead of unverified LLM vulnerability claims.
- Focus on accounting invariants, access control, reentrancy-state consistency, oracle assumptions, lifecycle constraints, and upgradeability risks.

Links: Code / demo coming soon

## Interests

- AI-assisted program analysis
- Smart contract invariant discovery
- Formal verification and SMT solving
- Fuzzing and counterexample generation
- Web3 security tooling
- Audit workflow automation

## Technical Stack

**Languages:** Python, TypeScript / Node.js, Solidity, Rust, C / C++

**Verification and Analysis:** Z3, SMT solving, bounded model checking, symbolic execution, property decomposition, invariants, fuzzing

**Web3 Security:** Foundry, Slither, Echidna, smart contract testing, DeFi security patterns, invariant testing

**AI Systems:** LLM agents, OpenAI / Anthropic APIs, tool calling, structured outputs, RAG, workflow automation

**Engineering:** Docker, GitHub Actions, APIs, backend systems, CI/CD, reproducible research artifacts

## Contact

Open to remote roles in Web3 security tooling, formal verification, AI-assisted audit workflows, and research engineering.

Contact: GitHub profile / email available upon request.
