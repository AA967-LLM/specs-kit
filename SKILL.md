---
name: speckit
description: Spec-Driven Development (SDD) workflow using Spec Kit. Use when building new features, refactoring major components, executing complex engineering tasks, or when the user mentions spec-kit or SDD.
---

# Spec-Driven Development (Spec Kit Workflow)

When building new features, refactoring major components, or executing complex engineering tasks, **do not write code immediately**. Follow this Spec-Driven Development (SDD) protocol:

## 1. Constitution Alignment (`/speckit.constitution`)
* **Objective:** Align with existing project standards.
* **Steps:**
  1. Check if `.speckit/constitution.md` exists in the project root.
  2. If it does, verify the architectural guidelines, tech stack guardrails, and styling conventions.
  3. If it doesn't, write/generate a draft constitution for the project.

## 2. Specification First (`/speckit.specify`)
* **Objective:** Define the system behavior and user stories before coding.
* **Steps:**
  1. Create a new specification file under `.speckit/specs/` (e.g., `.speckit/specs/user_auth.md`).
  2. Document target user stories, success metrics, UI/UX flows, and edge cases.
  3. Keep the focus on *behavior* and *interaction* rather than implementation details.

## 3. Ambiguity Resolution (`/speckit.clarify`)
* **Objective:** Identify and resolve missing constraints or risks.
* **Steps:**
  1. Inspect the generated specs for ambiguous logic, potential security flaws, performance bottlenecks, or missing details.
  2. Write down precise clarifying questions to ask the user.
  3. Adjust the specifications based on the user's feedback.

## 4. Technical Planning (`/speckit.plan`)
* **Objective:** Map out files, data models, and step-by-step task lists.
* **Steps:**
  1. Outline the proposed file structure, changes to existing files, database schemas, and API signatures.
  2. Detail the exact steps required for implementation.
  3. Document these in `.speckit/plans/` or append them to the spec document.

## 5. Task Decomposition & Execution (`/speckit.tasks` -> `/speckit.implement`)
* **Objective:** Build and verify step-by-step.
* **Steps:**
  1. Break the implementation down into small, isolated, trackable tasks.
  2. Execute one task at a time, implementing the code and immediately verifying it with tests (following TDD if specified).
  3. Make incremental commits or checkpoints for each task completed.
