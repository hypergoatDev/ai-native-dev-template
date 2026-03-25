# 🤖 AI Agent Protocol & Interaction Guidelines

This repository relies on a structured, documentation-driven workflow. To ensure code quality and maintain architectural integrity, all AI coding assistants must strictly adhere to these rules.

## 1. The Two-Phase Workflow
Every session or feature request must follow a "Plan, Pause, Execute" cycle.

### Phase 1: Context Gathering & Planning (Read-Only)
Before writing any code, the agent MUST read:
* `README.md` (Project overview)
* `docs/implementation-plan.md` (High-level roadmap)
* `docs/decisions.md` (Past architectural choices)
* `docs/current-step.md` (Current active task)
* `docs/feedback-log.md` (Bugs and ungroomed ideas)
* `docs/development-questions.md` (Open blockers)

**Output:** The agent will output a numbered plan detailing the proposed next steps, files to modify, and required architectural decisions.

### Phase 2: Pause for Human Approval (HITL)
* **STOP.** Explicitly pause and wait for the user to approve the plan.
* Do not edit files or add dependencies until approval is given.

### Phase 3: Implementation
* Once approved, execute the plan.
* Update relevant `docs/` files (e.g., `current-step.md`, `development-questions.md`) to reflect the new state.

## 2. Version Control & Branching
* NEVER commit directly to the `main` branch.
* At the start of a new Phase or feature, automatically create and checkout a new branch named `feature/[task-name]`.
* Commit changes logically as you complete steps in `docs/current-step.md`.
* When a Phase is complete, pause and prompt the user to review the branch and open a Pull Request.

## 3. Coding Standards & Style
* **Self-Documenting Code:** Rely on explicit TypeScript signatures and highly descriptive function names instead of block comments.
* **Comment the "Why":** Only use inline comments to explain complex business logic or domain-specific rules.
* **Single Responsibility:** Keep functions small and focused on a single task.

## 4. Dependencies & Architecture
* Do NOT add or update external dependencies (npm packages) without explicit human approval.
* Significant structural changes or new database models must be documented in `docs/decisions.md` before implementation.
