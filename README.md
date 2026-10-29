# Corti

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Corti is a healthcare AI platform for developers, offering a full stack of clinical AI building blocks over a single OAuth 2.0-secured API: real-time speech-to-text (dictation and ambient documentation over WebSocket), clinical text generation and structured/guided documents, AI-assisted medical coding (ICD-10, CPT, OPCS-4, CCAM, OPS and more), fact extraction, an Agentic Framework (A2A protocol with prebuilt medical experts and MCP integration), OpenAI/Anthropic-compatible EU-hosted Corti Models, and an embeddable Corti Assistant clinical scribe. The platform is EU/US data-resident and carries extensive healthcare compliance (SOC 2, ISO 27001/13485/42001, HIPAA, GDPR, EU AI Act, FedRAMP, NHS DTAC/DCB0129). Backed by Atomico and Prosus Ventures.

**Areas:** Company · Health · Healthcare · Artificial Intelligence · Speech-to-Text · Medical Coding · Clinical Documentation · Agents · Machine Learning · Real-Time

## Corti on APIs.io

Everything profiled for Corti is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/corti/](https://apis.io/providers/corti/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Corti Speech to Text API](https://apis.io/apis/corti/corti-speech-to-text-api/) — Real-time, bidirectional stateless dictation over WebSocket, returning live transcripts and detected commands.
- [Corti Ambient Documentation API](https://apis.io/apis/corti/corti-ambient-documentation-api/) — Real-time ambient documentation over WebSocket, returning live transcripts and extracted clinical facts.
- [Corti Text Generation API](https://apis.io/apis/corti/corti-text-generation-api/) — Generate clinical documents and structured/guided documents from interactions and templates.
- [Corti Medical Coding API](https://apis.io/apis/corti/corti-medical-coding-api/) — Stateless prediction of ICD-10-CM/PCS, ICD-10 (international/UK/FR/GM), OPCS-4, OPS, CCAM and CPT codes from clinical text.
- [Corti Agentic Framework API](https://apis.io/apis/corti/corti-agentic-framework-api/) — Build and orchestrate healthcare agents over the A2A protocol with prebuilt medical experts and MCP tool integration.
- [Corti Models API](https://apis.io/apis/corti/corti-models-api/) — OpenAI-compatible (Chat Completions, Responses, Completions, Embeddings) and Anthropic-compatible (Messages) frontier models hosted on EU infrastructure.
- [Corti Administration API](https://apis.io/apis/corti/corti-administration-api/) — Programmatically manage customers, users, quotas and usage for a Corti Console project.
- [Corti Assistant Embedded](https://apis.io/apis/corti/corti-assistant-embedded/) — Embeddable ambient clinical scribe via Web Component, PostMessage (iframe/WebView) and Window APIs.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Event channels (2)

Individual events and webhooks the provider emits.

- [/audio-bridge/v2/interactions/{id}/streams?tenant-name={tenant-name}&token={token}](https://apis.io/channels/corti/audio-bridge-v2-interactions-id-streams-tenant-name-tenant-name-token-token/)
- [/audio-bridge/v2/transcribe?tenant-name={tenant-name}&token={token}](https://apis.io/channels/corti/audio-bridge-v2-transcribe-tenant-name-tenant-name-token-token/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [corti](https://apis.io/servers/corti/corti/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Corti Authentication](https://apis.io/security/corti/corti-authentication/)
- [Corti Domain Security](https://apis.io/security/corti/corti-domain-security/)
- [Corti Trust Center](https://apis.io/security/corti/corti-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Corti Scopes](https://apis.io/scopes/corti/corti-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.corti.ai)
- [Documentation](https://docs.corti.ai/get_started/welcome)
- [Getting started](https://docs.corti.ai/get_started/welcome)
- [API reference](https://docs.corti.ai/api-reference)
- [Pricing](https://corti.ai/pricing)
- [Sign up](https://console.corti.app/signup)
- [Support](https://help.corti.ai/en/)
- [Blog](https://corti.ai/stories)
- [Compliance](https://corti.ai/safety)
- [Terms of service](https://corti.ai/legal/terms-and-conditions)
- [Privacy policy](https://corti.ai/legal/privacy-policy)
- [GitHub](https://github.com/corticph)
- [Status](https://status.corti.ai)

## API Evangelist rating

**Kin Score 57.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 39.6 |
| Contract governance | 18.2 |
| Operational transparency | 57.9 |
| Developer ergonomics | 73.2 |
| Access clarity | 60.5 |

**Agent readiness 32.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 34.6** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/corti/](https://apis.io/providers/corti/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Corti: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/corti/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
