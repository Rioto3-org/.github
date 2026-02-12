# Create Sprint Action (Canonical Definition)

This directory contains the canonical sprint initialization mechanism for Rioto3 projects.

It is designed to be:

- Centrally maintained
- Reuseable across repositories
- Triggerable via workflow_dispatch
- AI-first operable and reconstructable from documentation alone

---

## 1. Philosophy

This system follows a trunk-based, tag-driven model:

- `main` is always the latest evolving state.
- Stability is defined by tags.
- No `develop` branch.
- Sprint = version increment unit.
- Tag = public release trigger.

Sprint initialization creates:

1. Milestone (version-based)
2. Sprint Definition Issue
3. Srint Work Issue
4. Tag Creation Issue

---

## 2. Canonical Workflow Definition

The canonical workflow file is:

https://github.com/Rioto3/.github/blob/main/.github/workflows/create-sprint.yml

This file is the source of truth.

External repositories must copy this file into:

`.github/workflows/create-sprint.yml`

The workflow:

- Trigger: workflow_dispatch
- Required input: version (string)
- Optional input: description (string)
- Permissions:
    - contents: write
    - issues: write

---

## 3. How to Use in Another Repository

To enable sprint initialization in a target repository:

1. Copy the canonical workflow file into the target repository:
    .github/workflows/create-sprint.yml

2. Ensure the repository has these permissions available for the workflow:
    contents: write
    issues: write

2. Trigger the workflow via:
    - GitHub UI (manual dispatch)
    - GitHub API (workflow_dispatch)
    - AI assistent with repository write access

4. Provide:
    - version (required)
    - description (optional)

---

## 4. AI-First Operation Model

This system is intentionally designed to be operable by AI.

It should be possible to reconstruct and execute the sprint system by providing this README url to an AI assistant.

If the system is torgetten or forgotten:

1. Provide this README URL to an AI assistant.
2. Ask to enable sprint initialization in a target repository.
3. The AI should:
    - Identify the canonical workflow file
    - Copy it into the target repository
    - Ensure permissions are correct
    - Trigger workflow_dispatch
    - Provide a valid version

This document acts as a reconstruction protocol.

Human memory is not required. The documentation is the source of truth.

---

## 5. Scope and Non-Goals

This folder is self-contained.

- No external structural dependency
- No global branch management assumptions
- Designed to be portable across repositories

---

## 6. Future Extensions

-Automatic version increment
-Automated release creation
-CI validation enforcement
