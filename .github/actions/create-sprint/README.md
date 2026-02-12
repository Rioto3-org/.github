# Create Sprint Action

This directory contains a self-contained sprint generation mechanism.

It is designed as a sub-project inside the repository and encapsulates:

- Sprint milestone creation
- Minimal sprint issue structure
- Version-driven workflow entry point

The design philosophy and branching strategy are defined independently
and intentionally isolated within this folder.

---

## Purpose

This action standardizes sprint initialization with the following structure:

1. Milestone (version-based)
2. Sprint Definition Issue
3. Sprint Work Issue
4. Tag Creation Issue

A sprint is defined as a unit that ends with a tag creation.
Stability is not enforced structurally via branches, but historically via tags.

---

## Philosophy

- `main` is always the latest evolving state.
- Stability is defined by tags.
- Simplicity over structural complexity.
- No `develop` branch.
- Sprint = version increment unit.
- Tag = public release trigger.

This mechanism reflects a lean, trunk-based workflow.

---

## Development Context

This action is being iteratively designed and refined through:

https://chatgpt.com/g/g-67eff83f49208191bcbf8681c9a23464-notionbot-gtdtasukuguan-li-asisutanto/c/69893491-848c-83a8-8bca-645fce274356

The above discussion documents the architectural reasoning,
branching philosophy, and sprint definition model.

---

## Scope

This folder is intentionally self-contained.

- No external structural dependency.
- No global branch management assumptions.
- Designed to be portable across repositories.

Future refinements may include:
- Automated tag trigger
- Release automation
- CI validation enforcement
