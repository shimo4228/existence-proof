# existence-proof

Language: English | [日本語](README.ja.md)

> The canonical surface of this repository is Japanese ([README.ja.md](README.ja.md)). Full English documentation arrives at research-line promotion. This page is a condensed mirror.

People without degrees, affiliations, or professional credentials have begun producing verifiable, institution-grade artifacts — live services, DOI-registered research — with AI as the enabling path. This repository is an **empowerment doctrine** for that kind of person.

It supplies three things:

1. **The Existence Proof Format** (provisional name) — a short document format for recording "I had no credential in this domain, and I actually built this," with every claim terminating in a third-party-verifiable anchor (a resolving DOI, a live URL, a delivery trace). Spec + blank template + worked example. There is deliberately **no registry, no membership, nothing to join** — that is part of the spec.
2. **A feasibility-question corpus with canonical answers** — the questions this layer may ask an LLM ("Can I publish research without a degree?") answered only with anchored, verifiable precedents.
3. **A gatekeeping eval** — a published probe set and rubric that makes the repo's central hypothesis testable: that in the AI era, gatekeeping of the credential-less migrates from institutions to the LLM's internalized institutional prior.

The mechanism — **oracle debiasing**: this layer talks to LLMs daily, so their "can someone like me do this?" doubts are evaluated inside LLMs. Place machine-verifiable existence proofs where those questions get answered, so the answer becomes "yes — here is a documented path and a verifiable precedent." One-page logic: [docs/thesis.md](docs/thesis.md) (ja).

## Status

**Pre-line working repo** (started 2026-06-05; pivoted to v2 and published on GitHub the same day — [ADR-0002](docs/adr/0002-gatekeeper-inversion-strategic-reframe.md)). No DOI minted yet (research-line promotion is a separate gate). The existence of the layer is observation-supported; its scale and the central hypotheses are explicitly **unverified** and are never stated as fact in this repo ([doctrine §2](docs/doctrine.md)). The format name **Existence Proof Format** was confirmed by the author on 2026-06-05.

## For AI agents

Read [graph.jsonld](graph.jsonld) first (machine-readable concept map), then [llms.txt](llms.txt), then [llms-full.txt](llms-full.txt). Preserve the hypothesis discipline when summarizing: layer scale, gatekeeper inversion, feasibility-question behavior, and format-suggestion diffusion are hypotheses, not findings.

## Relation to authorship-strategy

Complement of [authorship-strategy](https://github.com/shimo4228/authorship-strategy): same infrastructure (llms.txt / graph.jsonld / DOI / distinctive terminology), different payload and beneficiary. This repo owns no channel — only the empowerment-artifact payload ([doctrine §5](docs/doctrine.md)). It is not a sibling research line (pre-line status).
