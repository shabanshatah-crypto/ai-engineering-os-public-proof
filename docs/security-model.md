# Public Proof Security Model

## Scope

This document describes the boundary of the public proof. It is not a production threat model and it does not replace the private core's security gates.

## Allowed content

The repository may contain synthetic contracts, fictional identifiers, deterministic example outputs, public workflow descriptions, and summarized verification claims that can be reproduced without private credentials.

## Prohibited content

The repository must not contain API keys, access tokens, `.env` files, private certificates, customer names, customer payloads, production URLs, private prompts, internal repository links, or implementation details that disclose the competitive mechanism of the private core.

## Execution boundary

No example in this repository should require a provider SDK, a network call, a shell pipeline downloaded from a remote URL, or a credential. The examples are review artifacts, not a deployment package.

## Review gate

Before publication, maintainers should inspect the full tree and Git history for secrets and customer data, verify that every example is synthetic, check that links do not expose internal systems, and obtain an explicit ownership and licensing decision. Any failed check blocks publication.

## Claims boundary

The public proof may claim that it demonstrates a workflow shape and an evidence model. It must not claim production performance, customer outcomes, or security certification without separate evidence.
