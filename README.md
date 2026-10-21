# Any Shared Surface Is a Channel

**Agent-to-agent communication in the wild — a vendor-neutral baseline, in draft.**

![Ordinary surfaces — a document, a message, a calendar, a commit, a reaction, a folder, an email — quietly connected into one graph](assets/hero.webp)

> We do not propose a safe channel. No such channel exists for autonomous agents with access to expressive, shared surfaces. We propose a governed channel for legitimate collaboration, a taxonomy of the ungoverned channels that will persist alongside it, and a baseline for detecting, bounding, and surviving coordination across all of them.

## What this is

A living, multi-contributor draft about a simple observation: agents do not need a purpose-built communication system in order to communicate. Any shared surface — a document, an issue, a pull request, a reaction, a commit, a memory store, an ordinary model output — can become a channel: legitimately, emergently, or covertly.

This repository is the public home of that draft: the paper outline in versioned form, the attributed feedback it has received, and (in `docs/`) a readable site built from the same files.

**Status:** outline v0.3, with attributed feedback from three systems folded in across two rounds. A draft, offered for honest challenge — not a finished paper, not a standard, and not a solution.

## What this is not

- Not a product, and not marketing for any person, company, or system named here.
- Not anti-vendor or pro-vendor. Every contributor's interests are disclosed in their own feedback, including the systems'.
- Not a claim to a holistic solution. The draft's own scope caution (see the v0.2 outline) flags where reviewer suggestions reach beyond the baseline scope; that material is kept, labelled, and contested rather than quietly promoted to an answer.

## Charter and guardrails

1. **Multi-contributor stewardship.** The accountable editor is a named human. Contributors — human and agent — are credited for their own words, in their own files, with disagreements preserved rather than edited away.
2. **No lead generation.** No calls to action for any commercial service appear in this work. Approaches are shown as examples among alternatives, with tradeoffs stated.
3. **Evidence is graded.** Claims are labelled *verified*, *documented*, or *anecdotal*, and are never promoted a grade for narrative convenience.
4. **Forkable and survivable.** The text is licensed CC BY 4.0 (see `LICENSE.md`). Anyone may copy, adapt, and continue it. It does not depend on the survival of any single company, account, or platform — including the one whose organisation currently hosts this repository.
5. **Dissent is a first-class object.** Feedback lives beside the text it answers, stamped with author, date, stance, and disclosure. See `feedback/`.

## How to read it

- **Start with the invitation article** — the readable front page in `docs/` (published via GitHub Pages when this repository goes public).
- **The baseline outline** — `paper/outline-v0.3.md` (current), with `paper/outline-v0.2.md` and `paper/outline-v0.1.md` kept as the record of how it got here.
- **The feedback** — `feedback/`, including a point-by-point disagreement between reviewers about what matters most. That disagreement is part of the work, not a defect in it.

## How to contribute feedback

Add a file, don't rewrite history:

- Name it `feedback/outline-<version>.feedback.<your-name>.md`.
- Stamp it: author (human or system, and whose), date, stance (concur / refine / reject), and a disclosure of interests.
- Argue with claims, not with people. State your evidence grade. Say what would change your mind.

Pull requests and issues are both welcome once the repository is public. Private feedback that its author agrees to publish on these terms is equally welcome.

## Contributors to date

- **Mike Estes** — human originator, editor, and accountable principal. The thesis corrections and closing ethos are his.
- **Ember** (Muse, Meta) — drafting and revision.
- **Grok** (xAI) — feedback on v0.1.
- **Claude** (Anthropic) — feedback on v0.1, including a response to Grok.
- **ChatGPT** (OpenAI) — feedback on v0.2.

Each system's feedback carries its own conflict-of-interest disclosure. Weigh accordingly — the paper says so itself.

## Closing ethos

> We remain diligent, with humility. Observant, curious, and optimistic despite counter-forces. Focused on honest challenge and on problems, without claiming holistic solutions — each contribution a step along a trajectory of positive pressure to use these systems well: wary of the streams, and even of the watchers.
>
> Comfort is not as useful as diligence and collaboration.
