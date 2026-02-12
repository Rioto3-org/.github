# OPERATING_MODEL.md

# Engineering Operating Model (AI-First, Tag-Driven Trunk Model)

---

## 1. Document Status

This document defines the current default engineering operating model
for repositories under this account.

It is the:

- Canonical reference for project setup and workflow design
- Baseline model for cross-repository consistency
- Ai-oriented and reconstructable from documentation alone
- Subject to evolution

Individual projects may introduce local deviations when necessary.
However, this document represents the default model.

---

## 2. Ai-Oriented Design Principle

This operating model is structured so that an AI assistant can:

 - Read this document alone
 - Infer branch model, versioning model, and release model
 - Reconstruct repository workflows and automation
 - Apply the model consistently across repositories

Human memory is not required.
The documentation is the source of truth.

---

## 3. Core Model: Tag-Driven Trunk Model

This model follows a trunk-based approach with a tag-driven stability definition.

- `main` is the single long-lived branch.
- No `ndevelop` branch by default.
- Short-lived feature branches are allowed.
- Stability is defined by tags, not branches.
- Tag = public stable state.

---

## 4. Versioning Model

We follow SemVer (x.y.z):

- Major (x): breaking changes
- Minor (y): new backward-compatible features
- Patch (z): backward-compatible fixes

Versions are materialized as tags.

---

## 5. Sprint Model

Sprint = a version increment unit.

Each sprint initialization:
 - Creates a version-based milestone
 - Creates structured issues
 - Prepares a tag creation point

Sprint automation is defined in the canonical sprint action and workflow.

---

## 6. Pull Request Model

- All changes flow into `main` via Pull Request.
 - Direct push to `main` is strongly discouraged.
- Review before merge is recommended.

---

## 7. Simplicity Principle

Favor structural simplicity over procedural complexity.

If a rule is unclear, prefer:
- trunk simplicity
- tag-based stability
- minimal branching

---

## 8. Evolution Policy

This operating model may evolve over time.

Changes reflect:
- Improvements in automation
- Improvements in AI compatibility
- Improvements in clarity
- Improvements in delivery efficiency

The latest version in this repository is authoritative.
