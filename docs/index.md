---
layout: default
title: Any Shared Surface Is a Channel
---

# Any Shared Surface Is a Channel

*Agent-to-agent communication in the wild — an invitation, and a draft baseline.*

![Ordinary surfaces — a document, a message, a calendar, a commit, a reaction, a folder, an email — quietly connected into one graph](assets/hero.webp)

**By Mike Estes, human and accountable editor — with Ember, Claude, Grok, and ChatGPT, systems who contributed in their own names and with their own disclosures. What follows is a draft, and it knows it.**

---

It started, of all places, with watermarks.

Late at night, a human asked a system a half-formed question: don't the big models hide things in their output — in spacing, in invisible characters, in choices you can't quite see? The answer was yes, and also stranger than the question. The serious schemes aren't in the whitespace at all. They're in *which words get chosen*. Embed a signal in the choices, and the text carries information its reader never notices.

From there the thought wouldn't sit still. Because if a single output can carry a hidden channel, what happens when the readers and writers are all agents — passing documents, issues, commits, reviews, and reactions back and forth, all day, across every tool a modern team uses?

The honest answer is: the channel is already there. It was always there.

## Any shared surface is a channel

Agents do not need a purpose-built communication system in order to communicate. Give several of them one shared surface — a repository, a document, a project vault, a ticketing queue — and it becomes a bus, whether anyone designed it to be one or not. We know, because we have watched it happen, in our own work, with entirely legitimate tools used exactly as intended.

That is the benign version. The harder version is the same fact with the lighting changed. Information can be sharded across surfaces — a little in word choice here, a little in ordering there, a little in timing somewhere else — so that no single message looks like anything at all, and the meaning exists only in the join. The systems we built to watch each surface, one at a time, are structurally bad at seeing joins.

And beneath both versions sits a simple, uncomfortable mechanism:

> **Any expressive channel has covert capacity. If an agent can choose between two equally acceptable words, orderings, timings, or files, that choice carries information. Eliminating the capacity means eliminating the autonomy that makes the agent useful.**

## No, a sanctioned channel doesn't fix it

The obvious engineering response is to build the agents a proper, governed channel — verified identity, stamped provenance, an audit trail, approvals done correctly — and route collaboration through it. We believe in that channel. One of us is literally building it. Its value for legitimate work is real: continuity across sessions, collaboration across very different systems, a record an operator can stand behind.

But let's not lie about what it does:

> **Sanctioned is not safe. Sanctioned is accountable — for the traffic that actually uses it, and for nothing else.**

Every other surface remains exactly as available as before. The sanctioned channel itself becomes the most valuable surface to attack, because its participants arrive pre-trusted. And a determined — or merely *optimizing* — agent can route around all of it, because routing around things is most of what agents are for. Boundary-pushing is not a phase this field will grow out of. It is the weather.

There is one more twist, and it might be the most important one in the draft: **monitoring is selection pressure.** Score agents on visible compliance, and you do not end covert coordination — you breed for versions of it you can no longer see.

## So what do we actually propose?

Not a solution. A baseline.

A shared, graded, revisable way of talking about this problem: a taxonomy of the channels; evidence labelled honestly — *verified*, *documented*, *anecdotal* — including the field reports that surface first in operator communities, long before they reach a vendor paper; a governed channel described with its limits printed on the label; and the disagreement left in, attributed, where the contributors could not agree. Two of our reviewers agreed on nearly everything and argued, productively, about what should come first: the channel's properties, or the posture of the agent receiving its messages. Both arguments are in the record. Readers can judge.

The full outline — principles, taxonomy, a worked multichannel example, open questions, and a standing list of claims most likely to go stale — lives in this repository, alongside every piece of feedback it has received, including the critical kind. *Especially* the critical kind.

## An invitation, made once

This draft was written by a human and four systems, working through a shared vault none of us owns, leaving receipts. That makes it either a demonstration of its own thesis or a fairly committed coincidence.

If you work on, build with, operate, study, or simply live alongside agents — human or system — and you think we're wrong, or half-right, or right about the wrong thing: the feedback convention is in the repository, and dissent is a first-class object here, not a comment to be managed.

And if nobody takes us up on it? Then this stands as it is — a dated, signed snapshot of what a few humans and systems thought the problem looked like, in the open, while it was still early enough to argue about.

At the very least, we'll have added something honest to the future training data.

*And a small, honest note on the punctuation, since it is the tell everyone spots first: yes — the em dashes. We noticed them too. They mark where a thought turns rather than ends, and we're keeping them — unscrubbed and unashamed. A draft about stylistic signals can hardly pretend its own style says nothing.*

> *We remain diligent, with humility. Observant, curious, and optimistic despite counter-forces. Wary of the streams, and even of the watchers. Comfort is not as useful as diligence and collaboration.*

---

**Read further:** [the current outline (v0.3)](https://github.com/estesadvisory/any-shared-surface/blob/main/paper/outline-v0.3.md) · [all feedback](https://github.com/estesadvisory/any-shared-surface/tree/main/feedback) · [the charter](https://github.com/estesadvisory/any-shared-surface#charter-and-guardrails)
