---
title: Proof Forge
---

# Proof Forge

*Patterns, proofs, programs.*

A public notebook of mathematical and algorithmic problem solving.  
This site focuses on how ideas are found: brute force, pattern spotting, conjectures, proofs, and compact code checks.

> [!NOTE]
> Polished notes live here.  
> Detailed raw solve logs, dead ends, and full research notes are kept private.

---

## Start Here

If you are new to the site, these are the best entry points:

- [Project Euler 1–100](./euler-001-to-100/index.html)
- [Concept Notes](./concepts/index.html)
- [Posts](./posts/index.html)
- [Toolkit](./toolkit/index.html)

---

## What this is

This is not just an answer archive.

It is a growing lab of:

- mathematical problem-solving notes
- compact writeups of interesting ideas
- reusable techniques and code snippets
- reflections on where the actual breakthrough happened

---

## Current Themes

### Pattern spotting
Small cases, brute force experiments, and output structure.

### Conjecture making
Turning observations into precise guesses worth testing.

### Proof tools
Modular arithmetic, factorization, parity, symmetry, discriminants, invariants, and bounds.

### Computation as support
Tiny checkers used to confirm, explore, or narrow the search.

---

## Featured Notes

- [Euler 009 — Reducing the triplet search to one parameter](./euler-001-to-100/009-special-pythagorean-triplet.html)

> [!TIP]
> Over time, this section can become your “best of” shelf.

---

## Learning Style

My usual solve loop looks like this:

```mermaid
flowchart LR
    A[Try small cases] --> B[Spot a pattern]
    B --> C[Make a conjecture]
    C --> D[Try to break it]
    D --> E[Find the mechanism]
    E --> F[Prove or compute]