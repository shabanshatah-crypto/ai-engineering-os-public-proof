# AI Engineering OS — Public Proof

This repository is a deliberately separated **Public Proof** for AI Engineering OS. It demonstrates the problem, the operating contract, the evidence model, and the security boundaries using synthetic data only. It does **not** contain the private runtime, orchestration implementation, customer integrations, credentials, or internal deployment configuration.

## The problem

AI engineering workflows often produce plausible output without a reproducible record of what was requested, which policies were applied, what was verified, and which artifact was released. Teams need a controlled path from discovery to execution, inspection, verification, and release evidence without coupling their product to a single model provider.

## The public example

The synthetic example in [`examples/synthetic-contract.json`](examples/synthetic-contract.json) describes a fictional `Order` API. The corresponding input and output show the kind of contract and evidence that a controlled workflow can expose without publishing its private implementation.

The public proof demonstrates five ideas:

| Capability | Public evidence |
|---|---|
| Workflow contract | A stable sequence from discovery to release attestation |
| Provider neutrality | No provider SDK, API key, or vendor-specific implementation is included |
| Evidence | Deterministic metadata and a reviewable result shape |
| Security boundary | Explicit refusal rules for remote shell execution, prompt bypasses, and literal secrets |
| Reproducibility | A small synthetic fixture that can be reviewed independently |

## What is intentionally not here

The private repository remains the source of the runtime and release implementation. This repository does not include `src/`, `application/`, `core/`, provider adapters, customer data, internal prompts, production configuration, or executable demo credentials. A public reader can understand the value and inspect the proof without reconstructing the private engine.

## Resources

| Document | Purpose |
|----------|---------|
| [`docs/one-pager.md`](docs/one-pager.md) | Quick overview for executives and investors |
| [`docs/architecture-diagram.md`](docs/architecture-diagram.md) | Visual system architecture and workflow diagrams |
| [`docs/case-study-template.md`](docs/case-study-template.md) | Template for documenting pilot results (private use) |
| [`docs/discovery-kit.md`](docs/discovery-kit.md) | Conversation guide for customer discovery |
| [`docs/security-model.md`](docs/security-model.md) | Security boundaries and prohibited content |

## Request a private pilot

A pilot should use one narrowly scoped workflow, synthetic or explicitly approved data, a fixed duration, a measurable baseline, and a reviewable artifact. Contact the maintainers with the workflow, current baseline, security constraints, and the success measure. No customer data should be sent through this public repository.

## Security

Read [`docs/security-model.md`](docs/security-model.md) before adapting the example. The security model is descriptive and does not claim that this repository is a production security boundary.

## Status

This is a review-ready public-proof candidate. It is intentionally kept separate from the private core. Ownership and publication approval have been confirmed for the contents of this repository; the private implementation remains excluded.

## License

This Public Proof is licensed under the [Apache License 2.0](LICENSE). The license applies only to the contents of this repository and does not grant access to, or permission to reproduce, the private AI Engineering OS implementation.
