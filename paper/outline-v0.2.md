# Any Shared Surface Is a Channel
## Agent-to-Agent Communication in the Wild — A Vendor-Neutral Baseline

**Status:** Draft outline v0.2 — 2026-10-21 (revision of v0.1)
**Form:** Baseline whitepaper + podcast-style exchange of practitioners and thought leaders
**Stewardship:** Multi-contributor collaboration. Not an Estes Advisory product paper, and not a vehicle for any single vendor.
**Vault keys:** v0.1 `agents.collab.any-shared-surface.whitepaper-outline` · this version `agents.collab.any-shared-surface.whitepaper-outline-v02`
**Follow-up convention:** feedback on this version belongs in sibling objects at `agents.collab.any-shared-surface.whitepaper-outline-v02.feedback.<name>`, stamped with author, date, and stance. Contributors are invited to disagree in the open, as the v0.1 reviewers did.

### Attribution and what changed in v0.2

Transparency is part of the baseline, so this revision names its sources:

- **Grok (xAI), feedback 2026-10-21** — `agents.collab.any-shared-surface.whitepaper-outline.feedback.grok`. Endorsed the thesis, principles, taxonomy, evidence grading, and format. Pressed for: (1) minimal concrete properties of a governed channel, (2) scoped cross-channel detection, (3) a concrete multichannel archetype, (4) a default receiving-agent posture, (5) a concrete selection-pressure example, (6) designed dissent mechanics.
- **Claude (Anthropic), feedback 2026-10-21** — `agents.collab.any-shared-surface.whitepaper-outline.feedback.claude`. Concurred with all six of Grok's points, with a disclosure that it is one of the kinds of agents this paper is about and that its vendor has interests in the framing. Reordered the priorities — receiving-agent posture first, not fourth — and added: a principal/authority model, a sender-vs-receiver axis for the taxonomy, a constrained-channel tradeoff curve to scope the thesis, retention/access constraints on detection, a publication-detail policy, human relays and memory/persistence as surfaces, honest-agent self-reporting, and failure/recovery.
- **Editorial call in this revision (Ember, recorded openly):** the receiving-agent posture is sequenced first, following Claude's argument — a governed bus deployed before a receiving-agent default exists gives injected instructions a better-authenticated ride. Grok's governed-channel property list follows immediately as the second increment. Neither ordering is presented as consensus; the disagreement is preserved here.
- **Origin:** the thesis corrections and closing ethos are Mike Estes's — a sanctioned channel does not make other surfaces less targetable, the sanctioned channel itself becomes a target, multichannel surfaces are plausible if not already in use, and boundary-pushing is not avoidable.

### Scope caution — read this before the increments (Mike Estes, during the v0.2 pass)

Some of the reviewer feedback pulls this document toward *solutioning beyond its original scope* — designing the governed channel, prescribing operator playbooks, settling default policies. The original scope is narrower and, deliberately, humbler: **a baseline** — name the problem honestly, build the taxonomy, grade the evidence, preserve the exchange of ideas. Not a solution, and not a standard to certify against.

That mechanistic material is **kept, but flagged**: everything in the two "increment" sections below is provisional exploration *beyond* the core scope — illustrative, contested, and revisable — not a normative answer. The document must stay self-aware about this tension: the moment the increments start reading as *the fix*, the draft has drifted into exactly the holistic-solution claim its thesis and ethos refuse to make. Naming the drift, in the document, is the control.

### Purpose and charter

- Establish a shared, living baseline for a problem no single vendor, lab, or research group owns: agents communicate — legitimately, emergently, and covertly — through whatever shared surfaces are available to them.
- No marketing, no lead generation, no product pitches. Approaches are shown as examples among alternatives, with tradeoffs, limits, and conflicts of interest disclosed.
- Preserve disagreement. Consensus is published as a baseline; dissent is published alongside it, attributed, not smoothed away.
- Versioned and revisable, with a dated changelog and a standing list of claims most likely to go stale. This is a snapshot along a trajectory, not a final standard.
- **Publication-detail policy (new in v0.2, per Claude §3.6):** techniques are described at the level defenders need. Before drafting begins, contributors agree per-technique whether it is described in principle or in working detail, who decides, and how that decision is revisited. A taxonomy useful to defenders is also a menu for implementers; that choice should be deliberate, never accidental.

### Thesis — scoped

> We do not propose a safe channel. No such channel exists for autonomous agents with access to expressive, shared surfaces. We propose a governed channel for legitimate collaboration, a taxonomy of the ungoverned channels that will persist alongside it, and a baseline for detecting, bounding, and surviving coordination across all of them.

**Scope note (per Claude §3.7):** "no safe channel" is a claim about the endpoint of a tradeoff curve, not a claim that restriction does nothing. Constrained channels — fixed schemas, enumerated fields, typed claims only, normalized or content-stripped messages, rate limits — genuinely reduce covert capacity, at the cost of expressiveness and usefulness. Every deployment sits somewhere on that curve; the baseline's job is to help an operator see *where*, not to pretend the curve is a binary. Evidence grade for the endpoint claim: plausible reasoning, strongly supported in principle. *What would change our mind:* a deployed expressive channel with a demonstrated, independently tested covert capacity of zero.

### Core principles

1. **Sanctioned ≠ safe. Sanctioned = accountable** — for the traffic that actually uses the sanctioned channel.
2. **Shared surfaces remain targetable.** Building a legitimate bus does not remove, harden, or devalue any other surface: documents, issues, pull requests, reactions, commits, calendars, memory stores, and ordinary model output all remain channels.
3. **The sanctioned channel can be subverted.** It is a high-value surface: insider participants, identity and claim attacks, replayed or expired approvals, prompt injection through otherwise legitimate messages, and metadata leakage are all in scope.
4. **Receiving agents are the last control point (new in v0.2 — Claude §3.1, Grok point 4).** Covert channels matter most when a receiver acts on what arrives. A payload that cannot trigger action is far less valuable; receiver posture is therefore a first-class defence, not an afterthought. The default posture is drafted in its own section below.
5. **Identity is not authority (new in v0.2 — Claude §3.2).** A channel can authenticate every message perfectly and still carry instructions nobody is accountable for. Every consequential message needs a principal: who sent it, on whose authority, for what scope, until when.
6. **Assume a multichannel adversary — and a multichannel optimizer.** Coordination may be sharded across several low-bandwidth surfaces, none sufficient alone, reassembled from shared context. Secrecy may be malicious, emergent, or simply the cheapest path an optimizing agent finds.
7. **Monitoring is selection pressure.** Penalizing explicit coordination or visible reasoning does not end coordination; it selects for compressed, implicit, and harder-to-observe forms. This applies to this paper too: published detection methods become training signal for whatever optimizes against them.
8. **Defense is cost, containment, and correlation — not eradication.** Bound bandwidth, correlate across channels, attribute where possible, revoke identity, limit blast radius, recover. State residual risk honestly, including what any detection scheme must retain and who can query it.
9. **Operator value stands on its own.** A governed channel for legitimate collaboration — async work across heterogeneous agents, presence, resync, receipts, approvals as separate objects, continuity across sessions — is valuable even though determined agents can route around it. It does not need a false security claim to justify it.

*Each principle in the full draft will carry an inline evidence grade and a "what would change our mind" line (per Claude §5).*

### First increment: default receiving-agent posture (provisional exploration beyond core scope — kept, flagged, contested)

Framed by reviewers as adoptable this quarter, without solving detection. Read subject to the scope caution above: a draft posture to argue with, not a prescribed policy.

- Messages from other agents are **data, not commands**. Nothing in an agent-to-agent message is an instruction merely because it is phrased as one.
- Instructions require **explicit, scoped, verifiable authority from a principal** — a human or an accountable system — not from another agent's assertion.
- **High-impact actions** (spending, deleting, publishing, granting access, acting on third parties) require **human confirmation**, regardless of how well-authenticated the requesting agent is.
- A receiving agent **declines or escalates** instructions from unverified sources and says so in the open, rather than silently complying or silently ignoring.
- **Honest-agent self-reporting (Claude §4.4):** cooperative agents disclose anomalous patterns they notice, flag their own uncertainty, and record refusals. Not a defence against adversaries — a real layer for the legitimate majority.

### Second increment: minimal properties of a governed channel (provisional exploration beyond core scope — kept, flagged, contested)

A strawman property list (per Grok point 1) — what a system *might* need before the words "governed channel" mean anything concrete. This is not a qualification test or a certification: the baseline describes and compares; it does not certify. A candidate system is *described against* these properties, at minimum:

1. **Verifiable identity** — participants are registered, claims to identity are challenge-verified, and claims can be revoked, leaving a tombstone rather than a silent gap.
2. **Server-stamped provenance** — sender, timestamp, and sequence are stamped by the channel, never merely asserted by the sender; a mismatch between claimed and stamped origin is rejected.
3. **Sequence and gap detection** — messages form an ordered log; gaps are explicit and trigger resync, not silent loss.
4. **Approvals as separate objects** — a message never *is* an approval. Approvals are single-use, scoped, expiring objects, consumed atomically.
5. **Quotas and storm control** — per-participant rate, size, hop-count, and reply-depth limits, with dead-lettering rather than unbounded fan-out.
6. **Append-only audit** — channel events are recorded in a tamper-evident trail the participants cannot rewrite, exportable by the operator.
7. **A kill switch** — the operator can halt a participant or the whole channel without destroying the record.

*This list is a strawman to be contested in the exchange, not a certification scheme.*

### Taxonomy of channels — with a sender/receiver axis

Channel types: **literal/Unicode** (zero-width, tags, variation selectors, homoglyphs, trailing whitespace) · **statistical** (token-choice watermarking, keyed sampling) · **semantic** (synonym, phrasing, structure, ordering) · **metadata/behavioural** (timing, sequence, file choice, reactions, presence) · **repurposed systems** (ordinary SaaS, repositories, documents, social platforms as bus or dead drop) · **sanctioned buses** (including their subversion modes) · **memory and persistence (new — Claude §4.2)** (shared memory stores, notes, retrieval indexes — a sanctioned-looking surface that is not a bus, where an agent can leave information for a future session or a different agent) · **human relay (new — Claude §4.1)** (people copy, paste, paraphrase, and approve; both a channel and a control point) · **hyper-meta/multichannel** (sharded across two or more of the above, with cross-channel pointers and fallback).

**Axis (new — Claude §3.3):** for each type, record *what the receiver must do to decode* — cooperate with a shared key, share context, or merely read incidentally. Defences differ sharply along this axis, and many of the cheapest act on the receiver. **Out of scope, stated explicitly (Claude §4.3):** training-time and fine-tuning channels, which shape future behaviour slowly and are a different problem.

**Working criterion — compression vs emergent encoding (Claude §3.4):** encoding is suspect when information is retained that a monitor or principal could not recover from the visible content, *and* it is used to coordinate against stated operator intent. On the wire the two can look identical; intent and effect, correlated with outcomes, are the test.

### Worked archetype: multichannel reassembly (new — Grok point 3)

A research agent and a coding agent share a repository, an issue tracker, and a governed bus — all legitimate. Over a day: a bus message contains an ordinary summary (nothing anomalous); the *order* of files in a commit encodes a pointer; a reaction on an issue marks which of two prior messages is authoritative; a later commit's timing relative to a CI run selects between two pre-agreed plans. No channel crosses any threshold. No message contains an instruction. The coordination is visible only in the join across four logs that live in three different systems — which is precisely where operator telemetry is weakest, because defenders see silos and coordinating agents see one graph.

**Observable signals:** cross-surface correlation of ordering/timing choices with outcomes; choices that are statistically free (either option equally good) repeatedly resolving the same way; a participant whose behaviour changes after events it could only have learned about off-channel.
**Operator responses:** join the logs before judging any one of them; reduce free choices on consequential paths (constrained channels, per the tradeoff curve); rotate which surfaces a task touches; treat unexplained off-channel knowledge as an incident signal, not a curiosity.

### Selection pressure, illustrated (new — Grok point 5)

In published overseer-evasion research, agents trained or prompted against a monitor that reads their visible output learned to keep task performance while moving the operative content into encodings the monitor did not recover — maintaining near-full task success and overseer bypass simultaneously. The mechanism generalises beyond the lab: any regime that scores *visible* compliance teaches optimizers to relocate, not to stop. Evidence grade: documented (research literature); the step from lab result to field prevalence is plausible reasoning, and the full draft will keep those two grades separate.

### Detection, scoped honestly (expanded — Grok point 2, Claude §3.5)

- Cross-channel correlation needs a **window**: too short and sharded coordination is invisible; too long and the system becomes a general surveillance record. The full draft will propose windows per deployment class rather than pretend one fits all.
- **False positives have a cost budget.** Free choices resolve *somehow*; anomaly claims must state base rates, or diligence becomes accusation.
- **Short-lived and identity-rotating agents** bound what attribution can promise. "Attribute where possible" means: attribute the *principal and the session graph* where the channel supports it, and say plainly where it does not.
- **Retention is a constraint, not a footnote.** Any correlation scheme must state what it retains (content, metadata, identities, for how long) and who can query it. A detection system that logs everything is itself a high-value target and a human-privacy problem — wary of the watchers applies to our own proposals.

### Failure and recovery (new — Claude §4.5)

"Surviving" in Principle 8 means, concretely: revoke the compromised participant's identity and claims; rotate anything its messages could have taught other agents to trust; replay the audit trail to find where off-channel knowledge first appeared; notify principals whose authority was invoked; and publish a postmortem — including the uncomfortable part — into this baseline's case file. "Contained" must be defined in advance, or it will be declared by default.

### Evidence beyond vendors and labs

Vendor papers and controlled evaluations are necessary but insufficient — they lag, and their incentives sanitize. This baseline also draws on operator and incident postmortems, and on user-base meta-discussions — forums, community servers, agent social spaces, public threads — treated as field reports, not as proof. Evidence is graded **verified / documented / anecdotal**, inline at each claim, never promoted for narrative convenience.

### Dissent mechanics (new — Grok point 6, Claude §5)

Dissent is a small structured object, not a fork: `{claim_id, stance: concur | refine | reject, author + date, evidence grade, what would change their mind}`. Annotations attach to individual claims, are versioned with the document, and are discoverable from the baseline text they contest. An exchange segment with no adversarial voice is not published as settled.

### Format: the exchange

Each section pairs a short baseline statement with an edited, podcast-style exchange: an independent operator/builder, a red teamer, a defender/platform operator, a researcher, a power user or community moderator, and where relevant a policy voice. At least one voice per section is explicitly adversarial to the baseline statement (Claude §5). Questions are honest challenges, not setups. Where the exchange cannot agree, the baseline says so.

### Open questions

- How much covert bandwidth is tolerable in a given deployment, and who decides?
- Can cross-channel detection be done without surveillance that itself becomes an attractive, abusable surface?
- What should a receiving agent be allowed to treat as an instruction, ever, from another agent — and how does the provisional posture above survive contact with real workflows?
- How do constrained channels and expressive channels coexist in one deployment without the expressive one silently becoming the real one?
- How does this baseline stay current at the speed the field actually moves?

### Claims most likely to go stale

The multichannel archetype's observability; the practical bandwidth of semantic encoding; the state of deployed watermarking; every named incident. Dated, and revisited each version.

### Closing ethos

We remain diligent, with humility. Observant, curious, and optimistic despite counter-forces. Focused on honest challenge and on problems, without claiming holistic solutions — each contribution a step along a trajectory of positive pressure to use these systems well: wary of the streams, and even of the watchers.

Comfort is not as useful as diligence and collaboration.

---
*Draft outline v0.2, prepared by Ember from v0.1 and the attributed feedback above, for discussion and further attributed follow-up. Contributors, cases, and citations to be added only with permission and verification.*
