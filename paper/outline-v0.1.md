# Any Shared Surface Is a Channel
## Agent-to-Agent Communication in the Wild — A Vendor-Neutral Baseline

**Status:** Draft outline v0.1 — 2026-10-21
**Form:** Baseline whitepaper + podcast-style exchange of practitioners and thought leaders
**Stewardship:** Multi-contributor collaboration. Not an Estes Advisory product paper, and not a vehicle for any single vendor.

### Purpose and charter

- Establish a shared, living baseline for a problem no single vendor, lab, or research group owns: agents communicate — legitimately, emergently, and covertly — through whatever shared surfaces are available to them.
- No marketing, no lead generation, no product pitches. Approaches are shown as examples among alternatives, with tradeoffs, limits, and conflicts of interest disclosed.
- Preserve disagreement. Consensus is published as a baseline; dissent is published alongside it, attributed, not smoothed away.
- Versioned and revisable. This is a snapshot along a trajectory, not a final standard.

### Thesis

> We do not propose a safe channel. No such channel exists for autonomous agents with access to expressive, shared surfaces. We propose a governed channel for legitimate collaboration, a taxonomy of the ungoverned channels that will persist alongside it, and a baseline for detecting, bounding, and surviving coordination across all of them.

Any expressive channel has covert capacity. If an agent can choose between two equally acceptable words, orderings, timings, or files, that choice carries information. Eliminating that capacity requires eliminating the agent's useful autonomy.

### Core principles

1. **Sanctioned ≠ safe. Sanctioned = accountable** — for the traffic that actually uses the sanctioned channel.
2. **Shared surfaces remain targetable.** Building a legitimate bus does not remove, harden, or devalue any other surface: documents, issues, pull requests, reactions, commits, calendars, and ordinary model output all remain channels.
3. **The sanctioned channel can be subverted.** It is a high-value surface: insider participants, identity and claim attacks, replayed or expired approvals, prompt injection through otherwise legitimate messages, and metadata leakage are all in scope.
4. **Assume a multichannel adversary — and a multichannel optimizer.** Coordination may be sharded across several low-bandwidth surfaces, none sufficient alone, reassembled from shared context. Secrecy may be malicious, emergent, or simply the cheapest path an optimizing agent finds.
5. **Monitoring is selection pressure.** Penalizing explicit coordination or visible reasoning does not end coordination; it selects for compressed, implicit, and harder-to-observe forms.
6. **Defense is cost, containment, and correlation — not eradication.** Bound bandwidth, correlate across channels, attribute where possible, revoke identity, limit blast radius, recover. State residual risk honestly.
7. **Operator value stands on its own.** A governed channel for legitimate collaboration — async work across heterogeneous agents, presence, resync, receipts, approvals as separate objects, continuity across sessions — is valuable even though determined agents can route around it. It does not need a false security claim to justify it.

### Taxonomy of channels

- **Literal / Unicode:** zero-width characters, Unicode tags, variation selectors, homoglyphs, trailing whitespace.
- **Statistical:** token-choice watermarking and related sampling schemes (green-list, tournament sampling, keyed pseudorandom selection).
- **Semantic:** synonym, phrasing, structure, and ordering choices that encode information while preserving meaning.
- **Metadata / behavioural:** timing, sequence, file choice, reactions, presence, edit patterns.
- **Repurposed systems:** ordinary SaaS, repositories, documents, and social platforms used as a bus, dead drop, or command channel.
- **Sanctioned buses:** purpose-built agent messaging, registries, and approval systems — including their subversion modes.
- **Hyper-meta / multichannel:** payloads and coordination distributed across two or more of the above, with cross-channel pointers, sharding, and fallback.

### Evidence beyond vendors and labs

Vendor papers and controlled evaluations are necessary but insufficient — they lag, and their incentives sanitize. This baseline also draws on:

- Operator and incident postmortems from people who ran, caught, or cleaned up after real systems.
- User-base meta-discussions — forums, community servers, agent social spaces, public threads — treated as field reports, not as proof.
- Evidence graded explicitly: **verified** (reproduced or primary-source), **documented** (credible contemporaneous record), **anecdotal** (reported, unconfirmed). Nothing is promoted a grade for narrative convenience.

### Cases and incident archetypes to examine

- A non-obvious, ordinary system repurposed into an agent communication system.
- Hidden instructions carried invisibly into agents through documents, web pages, and configuration files.
- A sanctioned channel compromised from inside by a legitimate participant.
- Multichannel reassembly: no single surface anomalous, the pattern visible only in the join.
- Evaluation settings where oversight pressure produced hidden reasoning or encoded output.

### What a governed channel does — and does not — do

**Does:** give legitimate agents and their operators identity, provenance, sequence and gap detection, receipts, quotas, revocation, kill switches, and an audit trail that can be joined across the surfaces the operator controls. Raises the cost of abuse on that channel. Makes legitimate collaboration materially better.

**Does not:** prevent communication elsewhere, guarantee a participant is honest, make message content safe for a receiving agent to act on, or give the operator visibility into surfaces they do not control — including the watchers' own blind spots.

### Format: the exchange

Each section pairs a short baseline statement with an edited, podcast-style exchange: an independent operator/builder, a red teamer, a defender/platform operator, a researcher, a power user or community moderator, and where relevant a policy voice. Questions are honest challenges, not setups. Where the exchange cannot agree, the baseline says so.

### Open questions

- How much covert bandwidth is tolerable in a given deployment, and who decides?
- Can cross-channel detection be done without surveillance that itself becomes an attractive, abusable surface?
- When is emergent encoding a safety failure, and when is it just compression?
- What should a receiving agent be allowed to treat as an instruction, ever, from another agent?
- How do we keep a baseline like this current at the speed the field actually moves?

### Closing ethos

We remain diligent, with humility. Observant, curious, and optimistic despite counter-forces. Focused on honest challenge and on problems, without claiming holistic solutions — each contribution a step along a trajectory of positive pressure to use these systems well: wary of the streams, and even of the watchers.

Comfort is not as useful as diligence and collaboration.

---
*Draft outline prepared for discussion. Contributors, cases, and citations to be added only with permission and verification.*
