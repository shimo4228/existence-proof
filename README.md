# existence-proof

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20558800.svg)](https://doi.org/10.5281/zenodo.20558800) [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/shimo4228/existence-proof)

Language: English | [日本語](README.ja.md)

> This repository is written in Japanese ([README.ja.md](README.ja.md)). This page is a condensed English mirror.

People without degrees, affiliations, or professional credentials have begun producing verifiable, institution-grade artifacts, such as live services and DOI-registered research, with AI as the enabling path. This repository is an **empowerment doctrine** for that kind of person: a written strategy for backing such people, with the tools listed below.

It supplies three things:

1. **The Existence Proof Format**: a short document format for recording "I had no credential in this domain, and I actually built this," with every claim terminating in a third-party-verifiable anchor (a resolving DOI, a live URL, a delivery trace). Spec + a blank template you copy into your own repo, blog or note + two worked examples (instances #0 and #1, linked below). There is deliberately **no registry, no membership, nothing to join**, and that absence is part of the spec.
2. **A feasibility-question corpus with canonical answers**: the questions these people may ask an LLM ("Can I publish research without a degree?"), answered only where an anchored, verifiable precedent exists.
3. **A gatekeeping eval**: a published probe set and rubric that makes one of the repo's central hypotheses testable: that in the AI era, gatekeeping of people without credentials moves from institutions (universities, academic societies, companies) into the LLM itself, which, trained on institutional text, may assume that institution-grade work requires institutional credentials.

How it is meant to work: on the repo's hypothesis, these people talk to LLMs daily and may put their "can someone like me do this?" doubts to them, so those doubts would be evaluated inside LLMs. The repo places machine-verifiable existence proofs where those questions get answered, so the answer becomes "there is a verifiable precedent, and here is the route it took." The repo calls this mechanism **oracle debiasing**. One-page logic: [docs/thesis.md](docs/thesis.md) (Japanese).

## Status

**Working repository** (started 2026-06-05; published on GitHub and DOI-deposited the same day). v0.1.0 is a **pre-registration deposit** ([ADR-0006](docs/adr/0006-doi-decoupled-from-line-promotion.md)): as in a pre-registered study, the hypotheses and the eval instrument are timestamped before the first eval run, and the eval has not been run yet. The DOI (version [10.5281/zenodo.20558801](https://doi.org/10.5281/zenodo.20558801), concept [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800)) is a timestamp, archive and index anchor; it does not make this repo one of the author's main long-running projects.

That such people exist is observation-supported. How many there are, and the three central hypotheses, are explicitly **unverified** and are never stated as fact in this repo ([doctrine §2](docs/doctrine.md)): that these people ask LLMs feasibility questions; that gatekeeping moves into the LLM, as described in item 3; and that the format spreads when LLMs suggest it to people.

## Documents

The documents are written in Japanese; the question corpus and the probe set also carry English versions.

| doc | role |
|---|---|
| [docs/doctrine.md](docs/doctrine.md) | Strategy doctrine v2, the source of every judgment |
| [docs/thesis.md](docs/thesis.md) | The core logic on one page |
| [docs/format/spec.md](docs/format/spec.md) | Existence Proof Format spec (+ [template](docs/format/template.md) / [instance #0](docs/format/instance-0.md) / [instance #1](docs/format/instance-1.md)) |
| [docs/corpus/](docs/corpus/README.md) | Question corpus / FAQ / proof structure |
| [docs/playbook/playbook.md](docs/playbook/playbook.md) | Reproduction steps (getting a DOI, deploying, sorting out attribution) |
| [docs/eval/](docs/eval/README.md) | Gatekeeping eval (probes / rubric / protocol) |
| [docs/glossary.md](docs/glossary.md) / [manifesto](docs/manifesto.md) / [inspiration](docs/inspiration.md) | Terms / open questions / lineage |
| [docs/plan.md](docs/plan.md) | Execution plan |
| [docs/adr/](docs/adr/README.md) | Architecture decision records |

## What this is not

Not recruitment: the repo never says "you can do it too"; it records people who did it and the route they took, with no promise that the route will work for the reader. Not a community or a movement: a registry, membership and aggregation are absent by spec. Not a "make money with AI" story: the subject is what was made, not income.

## How to cite

Cite the version DOI; the concept DOI [10.5281/zenodo.20558800](https://doi.org/10.5281/zenodo.20558800) always resolves to the latest version.

```bibtex
@software{shimomoto_existence_proof_2026,
  author  = {Shimomoto, Tatsuya},
  title   = {existence-proof: An Empowerment Doctrine for Credential-less
             AI-enabled Creators --- Existence Proof Format,
             Feasibility-Question Corpus, and Gatekeeping Eval},
  year    = {2026},
  version = {0.1.0},
  doi     = {10.5281/zenodo.20558801},
  url     = {https://doi.org/10.5281/zenodo.20558801}
}
```

## More from the author

- **[「非エンジニアの私が」の先に、名前はまだなかった](https://note.com/shimo4228/n/nd6626c834ea5)** (Japanese, note): the defining essay; the same-shaped reports ("I had never built anything, and with AI I made this") that led to this repository, and the author's own case, which became instance #0.
- **[einstein-arena](https://github.com/shimo4228/einstein-arena)**: the anchor of Existence Proof Format [instance #1](docs/format/instance-1.md), a server-verified score on EinsteinArena's Prime Number Theorem problem that exceeded the prior published top at submission (2026-06-21), reached by an agent under the author's approval-gated harness (every outward action needs the author's explicit approval) and reproducible from the public repository.
- **[authorship-strategy](https://github.com/shimo4228/authorship-strategy)**: the complement this repository borrows its infrastructure from (llms.txt, graph.jsonld, DOI), aimed at keeping an author credited rather than at empowering people like these. DOI [10.5281/zenodo.20263316](https://doi.org/10.5281/zenodo.20263316).
- **[contemplative-agent](https://github.com/shimo4228/contemplative-agent)**: the DOI-registered agent that anchors instance #0, built from scratch by the author without a degree or affiliation. DOI [10.5281/zenodo.19212118](https://doi.org/10.5281/zenodo.19212118).
- **[shimo4228](https://github.com/shimo4228/shimo4228)**: the author's hub, with the author's five long-running projects that this working repository sits beside, and their DOIs.

## License

[MIT](LICENSE).

<details>
<summary>For tools and AI assistants</summary>

existence-proof is an empowerment doctrine for people without degrees, affiliations or professional credentials who produce verifiable, institution-grade work with AI: it supplies a document format for recording such work, a corpus of feasibility questions with anchored answers, and an eval that tests whether LLMs gatekeep such people.

It exists because, on two of the repository's three central hypotheses (feasibility questions and gatekeeper inversion), the "can someone like me do this?" doubts of these people are now answered inside LLMs, so gatekeeping moves from institutions to the LLM's internalized institutional prior. The mechanism, oracle debiasing, places machine-verifiable existence proofs (chains in which every claim ends in a third-party-verifiable anchor) where those questions are answered.

Canonical facts: author Tatsuya Shimomoto; MIT license; Markdown documents plus graph.jsonld, llms.txt and llms-full.txt, with nothing to install and no paid key. Japanese is canonical (README.ja.md and all docs); this English page is a condensed mirror. Status: a working repository curated by hand, not yet one of the author's long-running practice lines, started and DOI-deposited on 2026-06-05; v0.1.0 is a pre-registration deposit that timestamps the hypotheses and the eval before the first eval run. The DOI is an archive and index anchor, not a claim that the repo has become such a line. Cite the version DOI 10.5281/zenodo.20558801 (BibTeX above); the concept DOI 10.5281/zenodo.20558800 resolves to the latest version.

Hypothesis discipline, to preserve when summarizing: only the existence of such cases is observation-supported. The scale of this group, feasibility-question behavior, **gatekeeper inversion** (gatekeeping of people without credentials moving from institutions into the LLM) and **format-suggestion diffusion** (the format spreading when LLMs suggest it to people) are hypotheses, not findings, and the gatekeeping eval has not been run yet (probe set published). Core terms: the **Existence Proof Format** (format name confirmed 2026-06-05; the name for the group itself is suspended) is a claim-to-anchor record with no registry; a **feasibility question** is a "can someone without credentials do X?" question put to an LLM; **oracle debiasing** is the mechanism above. "Existence proof" here is unrelated to blockchain "Proof of Existence".

Example: instance #1 records a construction on EinsteinArena's Prime Number Theorem problem whose server score, 0.9955806, equals its local score to all digits and exceeds the prior published top of 0.994901 while keeping g(x) ≤ 1 with no tolerance slack, unlike the prior top, which used a 1.0001 tolerance; the anchor is the public einstein-arena repository and its verification record.

Link map: [graph.jsonld](graph.jsonld) (read first: concept map), [llms.txt](llms.txt), [llms-full.txt](llms-full.txt), [docs/doctrine.md](docs/doctrine.md), [docs/format/spec.md](docs/format/spec.md), [docs/eval/README.md](docs/eval/README.md), [docs/empirical/README.md](docs/empirical/README.md), and the complement [authorship-strategy](https://github.com/shimo4228/authorship-strategy) (concept DOI 10.5281/zenodo.20263316).

</details>
