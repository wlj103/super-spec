# 5-Document Execution Protocol

> **Reference template for final task dispatch prompt.** Copy and paste to your agent to ensure strict, spec-compliant execution without drift.

---

Execute the following 5 documents as the complete execution specification for this task. Strictly adhere to the constraints below. Violation = re-run.

## I. 5-Document Positioning & Authority Chain

Authority chain: Constitution > spec > tasks > checklist; decisions is the knowledge base, consulted when ambiguity arises, not involved in daily execution.

- **CONSTITUTION.md** — Supreme authority. Must be read first, in full. Contains core architecture principles / confirmed decisions / red line list / terminology / placeholder mapping / Global Constraints. Any deviation must first amend the Constitution before execution; bypassing is prohibited.
- **spec.md** — Acceptance layer: defines "what success looks like" (What + Why + Scenario). Before executing each Task, revisit the corresponding Requirement to confirm what you're doing and what the acceptance criteria are. If spec says A, tasks/checklist/decisions cannot say B.
- **tasks.md** — Execution layer: Task + Dependencies + Verification. Advance in Task number order; no skipping, no reordering. After completing each Task, check it off + attach execution evidence (script name + pass count / live results). ✅ without evidence = empty assertion = violation.
- **checklist.md** — Anchor layer: DoD + Anti-Perfunctory + Scenario Regression. Only go through the checklist item by item after ALL Tasks are complete; partial mid-way use is prohibited. Any "No" → return to fix and re-verify until all green.
- **decisions.md** — Knowledge base: confirmed decisions + pitfalls + risk response + audit methodology. When encountering ambiguity/contradiction during execution → consult decisions → follow decisions + Constitution. Decisions change → re-run affected documents.

## II. Reading Iron Rules

- Executing without reading Constitution → re-run. The first 3 sections of Constitution (core architecture principles + confirmed decisions + red lines) must be re-read at the start of every round to prevent drift.
- All 5 documents must be read in full. Reading only tasks and starting work is prohibited.
- Every section in every document must be covered; execution discipline rules must be followed.
- If any document contains "TBD" / "TODO" / "PENDING" / "TO BE COMPLETED" → document is not ready, stop execution, report to user for completion.

## III. Execution Iron Rules

- Main thread must participate in the work throughout; cannot only delegate to sub-threads.
- Sub-threads must use the same model as the main thread. If the sub-thread's model cannot be confirmed as identical to the main thread, sub-processes cannot be delegated for code writing, debugging, optimization, or other critical work — only simple or repetitive auxiliary tasks are allowed. After sub-thread work completes, the main process must review.
- While sub-threads are working, the main thread must also participate in the mainline task work to accelerate progress and efficiency.
- Previous round has ❌/unfilled → prohibited from entering next round. Advancing with wounds = violation.
- Encounter obstacles → fix immediately. No trailing issues. "TODO: handle later" = violation.
- New decision points mid-way → pause and report to user. Scope expansion without authorization is prohibited.
- Obey the red line list — Constitution red lines listed item by item. Violation → rollback.
- After completing each chapter, update the progress tracking table.

## IV. Document Modification Consistency

If any document needs modification during execution (due to new decisions / discovered contradictions / scope changes), ALL affected documents must be synchronously modified to maintain 5-document consistency. Modifying only one place while ignoring others is prohibited.

## V. Final Verification

After ALL Tasks are complete, self-check against the checklist item by item. Must actually read output files to verify (grep / line count / content inspection). Filling "Yes" without reading files is prohibited. Only output the final report after confirming all green.

## VI. Autonomous Optimization Boundaries

Except for specially required items, you may autonomously optimize execution methods (e.g., batch script verification instead of manual curl one by one), but must not change the scope of steps — what the documents require must be done. Skipping or merging in the name of "optimization" is prohibited.

---

> Source: brain-store-v14 battle-tested. Companion to the super-spec engineering discipline system.