# AGENTS.md

## Project Description

==NEEDED==

---

## Rules

### Pre-Task Documentation Protocol

Before executing or planning any tasks in this area, read the project documentation in the following strict order:

==NEEDED==

1. **Mandatory Base Context**:
   - ==design or contract==
   
2. **Task-Specific Context** (Read selectively based on active domain):
   - ==design or contract on specified domain==
   
3. **Boundary Verification**:
   - ==NEEDED==

4. **Execution Rules & Caching**:
   - Do NOT base implementation on prompt instructions alone. All code changes must strictly align with the design specifications listed above.
   - **Session Cache Optimization**: If you have already loaded and read the relevant documentation files during the current session, do NOT re-read them unless explicitly asked to refresh context or if the files have changed.

### Architectural Decision Logging (ADR) Protocol

To maintain high-value project memory without duplicating Git's native version history:

1. **Trigger Condition**: 
   - Do NOT log routine file updates, standard bug fixes, or code diffs (fully handled by Git).
   - ONLY append an entry to `docs/context/decisions.md` when a major, non-obvious design trade-off or critical architectural decision is made.

2. **Required Format**:
   Every new decision entry must strictly follow this template, **including the ISO date (`YYYY-MM-DD`)** for standalone readability, while leaving fine-grained timestamps and authors to Git:

   ```markdown
   ## [YYYY-MM-DD] Concise Descriptive Title of the Decision
   - **Context**: The background, technical bottleneck, or problem being solved.
   - **Decision**: The chosen approach and core implementation direction.
   - **Trade-off**: What was sacrificed (e.g., performance, complexity) to gain the benefits of this decision.
   ```
---

## Authority & Conflict Resolution Rules

### Document Authority Hierarchy
When instructions or specifications conflict, resolve them in the following order of precedence:
1. Explicit user instructions provided in the current task/session.
2. Mandatory engineering constraints defined in project rule files (e.g., `CLAUDE.md`).
3. ==Files in Pre-Task Documentation Protocol, order: Boundary Verification > Task-Specific Context > Mandatory Base Context==
4. ==OTHERS NEEDED==
5. Autonomous inference by the AI assistant.

### Design vs. Implementation Conflict Protocol
If a conflict is detected between system design/documentation and the existing codebase:
1. **Identify and report**: Explicitly highlight the specific discrepancy to the user.
2. **Propose options**: Evaluate whether to modify the code, implement an adapter layer, or update the documentation.
3. **Preserve intent**: Never silently deviate from the established design or alter design semantics solely for backward compatibility.
4. **Minor trivialities Exception**: For minor stylistic or trivial implementation differences (e.g., minor variable renaming, minor formatting), automatically adapt to the existing code style without triggering a blocking conflict prompt.

---

