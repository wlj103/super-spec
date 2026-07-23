---
name: super-spec
description: Seven-Gate engineering discipline for AI agents: anti-corner-cutting, evidence-based verification, spec-first, five-document interlocking. For Claude Code, Cursor, Codex, and all AI coding agents. Trigger: "spec", "production-grade", "don't cut corners", "anti-corner-cutting".
license: MIT
---

# Super-Spec

**Make AI agents walk through seven verification gates before delivery — not just give you an answer that "looks fine."**

## The Problem

AI coding agents are technically brilliant but behaviorally undisciplined. They skip steps, fill in defaults without asking, claim "tests passed" without evidence, and confidently deliver results that break in production. Traditional prompt engineering fails because models learn to circumvent prompts — "enforce verification rigorously" becomes four words in the output: "Verification enforced rigorously."

Super-Spec is not a prompt. It is not a template. It is a **structural enforcement system** — a complete engineering discipline that compels AI agents to walk through every step, produce verifiable deliverables, and hand you **verified, production-grade results**.

## What Makes This Different

Super-Spec is the only skill in the ecosystem that systematically catalogs **how models cut corners** and creates **operational definitions** to prevent each tactic. Other spec tools tell the agent what to produce. Super-Spec prevents the agent from producing garbage and calling it done.

| Other Spec Tools | Super-Spec |
|-----------------|------------|
| "Write a spec" | Seven gates the agent must pass through; no skipping |
| Trust the agent to follow instructions | Structural locks: grep-able checklists, cross-document Scenario IDs, non-repudiable evidence |
| Agent declares "done" | Gate Five: DoD Final Verification with spot-check re-verification |
| "Tests passed" | Evidence required: script name + pass count + live e2e results |
| Human review as quality gate | Five-document interlocking substitutes team review for solo developers |

## Six Design Principles

1. **Constrain behavior, not capability** — Don't instruct the model on what it already excels at (architecture, design). Lock down what it shortcuts: exhaustive coverage, evidence, bidirectional links.
2. **Structural locks, not prompt gates** — Prompts can be circumvented. Only grep-able checklists, cross-document-consistent Scenario IDs, and non-repudiable evidence truly lock things down.
3. **Divide-and-conquer interlocking** — Five documents, each with a distinct responsibility, cross-validate each other. If spec says A, tasks cannot say B.
4. **Constitution-driven, not memory-driven** — Consistency comes from the Constitution document being written down, not from "the model remembers."
5. **Probe-driven, not hard-coded** — Ports, paths, dependencies, and red lines are discovered at runtime. Change environments without touching the skill.
6. **Evidence-based verification, not trust-based** — "Looks fine" does not count. Spot-check three ✅ items using a different method in the final round.

### How Models Circumvent Instructions

| You say | It does |
|---------|----------|
| "Enforce verification rigorously" | Writes: "Verification enforced rigorously" |
| "Cover everything exhaustively" | Omits 3 items, writes "others similar" |
| "Provide test evidence" | Writes: "Tests passed" with zero evidence |
| "Don't hard-code" | Hard-codes the path and pretends it didn't |

---

## Seven-Gate Pipeline

```
Requirements → G0: Anchor Review → G1: Decision Points → G2: Constitution
→ G3: Five-Document Generation → G4: Progressive Execution
→ G5: DoD Final Verification → G6: Wrap-Up → Delivery
```

| Gate | Prevents | Pass Condition |
|------|----------|----------------|
| **G0: Anchor Review** | Acting without understanding current state | Code facts + confirmed decisions + no-change list, user-confirmed |
| **G1: Decision Points** | Agent filling in defaults on its own | Unconfirmed items prohibited from defaulting; ask user item by item |
| **G2: Constitution** | Understanding drift across sessions | Seven required sections written; five documents implicitly inherit |
| **G3: Five-Document Generation** | Cutting corners, skipping steps, empty verification | Anti-Corner-Cutting Clause + 18-item verification checklist |
| **G4: Progressive Execution** | Declaring completion after one round | ≥3 progressive rounds; all P0 green before proceeding |
| **G5: DoD Final Verification** | Self-deceptive verification | Item-by-item evidence + spot-check 3 ✅ items via different method |
| **G6: Wrap-Up** | Omissions, residual garbage | 12-item wrap-up checklist, verified item by item |

**Not "recommended." Not passable without completing.**

---

## Five-Document Interlocking System

```
CONSTITUTION.md  ← Supreme authority; drives everything
      ↓ Implicit inheritance
spec.md          ← What + Why + Scenario (acceptance layer)
      ↔ Bidirectional links
tasks.md         ← How + Dependencies + Evidence (execution layer)
      ↔ Bidirectional links
checklist.md     ← Verify + DoD + Anti-Perfunctory (anchor layer)
      ↕ Ambiguity fallback
decisions.md     ← Decisions + Pitfalls + Risk Response (knowledge base)
```

Each document has a distinct responsibility. Cross-validation catches drift: Scenario IDs must match across all five documents. Base changes trigger diff updates.

---

## Trigger Conditions

- New project / new core module / new service / major version upgrade
- User says "spec", "disciplined execution", "don't let the AI cut corners"
- User wants to convert an existing design document, requirements document, or prompt document into a structured, verifiable execution plan

## Prerequisites

At least one of the following must already exist:
- Complete design document (architecture design, technology selection, upgrade roadmap)
- Requirements document (functional requirements, acceptance criteria, constraints)
- Development document (API design, data model, interface specification)
- Prompt document (agent behavior specification, execution discipline, output format)

This skill **does not create requirements from thin air** — it transforms existing design documents into a structured five-document system and hands them to an agent for disciplined execution.

---

## Iron Rules

Violation of any rule → redo from the point of violation.

| # | Rule | Why (Behavioral) | Violation Example |
|---|------|------------------|-------------------|
| 1 | Did not read template before generating document → redo | Models skip reading templates and generate directly | Writing spec without reading Constitution template |
| 2 | Unconfirmed decision points prohibited from defaulting → ask user | Models fill in defaults silently | "Default to SQLite" without asking |
| 3 | Merging sections prohibited — each section outputs independent summary | Models merge to save effort | "Gates Three, Four, Five merged output" |
| 4 | Skipping sections prohibited | Models skip "unimportant" sections | Skipping Impact analysis, writing Task directly |
| 5 | Passing without evidence prohibited — must provide execution evidence | Models say "looks fine" | Checklist all "Yes" with no evidence |
| 6 | After each section: clean temp files → log changes → update progress | Models skip wrap-up steps | Finishing without logging; next round doesn't know what changed |
| 7 | Previous round has ❌/unfilled → prohibited from entering next round | Models push forward with wounds | R1 has 2 ❌, directly enters R2 |
| 8 | Encounter obstacles → fix immediately, no trailing issues | Models mark "TODO: later" to bypass | "TODO: test in production" |
| 9 | Obey template red lines (dynamic paths, single token source, no silent logging) | Models hard-code, fail silently | Hard-coding `/home/user/` path |

---

## Gate Zero: Anchor Review

**First step** — understand current state before discussing design. Output an "Anchor Checklist":

1. **Current Code Facts**: Existing utility functions, data structures, API parameters, auto-update chains — each with location + impact on design
2. **Confirmed Historical Decisions**: From project memory, historical specs, or previous user statements
3. **Explicit No-Change List**: Modules, files, or logic that must not be touched this round

Example:
```
Current Code Facts:
- core/writer.py: write_batch() already implements dedup + version chain (no change; call only)
- config.py: ports/paths read from .env (3 new env variables added this round)

Confirmed Historical Decisions:
- 2026-07-20: Dependencies reduced from 14 to 10; torch untouched

Explicit No-Change List:
- core/searcher.py — no change this round
- faiss index structure — no dimension change
```

Proceed to Gate One after user confirmation.

---

## Gate One: Decision Point Extraction

Output two items:

1. **Requirement Understanding Summary**: One-sentence positioning + core constraints
2. **Decision Point List**: Each item with 2-4 candidates + recommendation

Example:
```
D1: Dependency reduction scope
  A) Remove only Rerank package (low risk, medium benefit) ← Recommended
  B) Replace torch with lightweight alternative (high risk, large benefit)
  C) No dependency changes (zero risk, zero benefit)
```

Present in batches using **AskUserQuestion** (max 4 per batch).

---

## Gate Two: Generate Constitution

After all decisions confirmed, generate Constitution → `{project}/specs/{change_id}/CONSTITUTION.md`.

### Required Sections

| Section | Content | Correct | Counterexample |
|---------|---------|---------|----------------|
| **Project Name + Positioning** | One sentence | "V14 Brain Memory Architecture Upgrade: R2.5 Dependency Reduction + Graph Suite" | "Upgrade" |
| **Core Architecture Principles** | 3-6 non-negotiable principles | "Progressive Rule: R1 scan → R2 review → R3 root-cause; restart after any code change" | "Follow architecture principles" |
| **Confirmed Decisions** | All Gate One conclusions + rationale | "D1 chose A: Remove only Rerank, because torch is a V13 red line" | "D1 chose A" (no rationale) |
| **Red Line List** | Boundaries never to be crossed | "torch/transformers/safetensors untouched; faiss dimension unchanged" | "Core logic unchanged" |
| **Core Terminology** | Precise definitions + cross-module mappings | "supersede = versioned replacement: old marked expired, new appended; queries follow pointer to latest" | "supersede is a replacement mechanism" (circular) |
| **Template Placeholder Mapping** | `{{PLACEHOLDER}}` → actual value | "`{{DB_PATH}}` → `config.get('database.path')`" | "`{{DB_PATH}}` → `/data/db`" (hard-coded) |
| **Global Constraints** | Project technical facts the model cannot guess | (see below) | (see below) |

### Global Constraints

These are **facts**, not rules — version numbers, path conventions, credential retrieval methods. The model cannot guess them. Every Task implicitly inherits them.

```markdown
## Global Constraints

- Language Version: Python ≥ 3.11 / Node ≥ 18
- Database Mode: SQLite WAL + busy_timeout / PostgreSQL connection pool limit
- Path Resolution: Resolve from configuration root; hard-coded absolute paths prohibited
- Credential Source: Environment variables first, .env fallback; plaintext prohibited
- Logging Standard: stdout/stderr redirected to designated directory
- Encoding: Windows scripts GBK+CRLF / Unix UTF-8+LF
```

### Placeholder Rules

1. Templates uniformly use `{{PLACEHOLDER}}`; never write literal values
2. First execution step: read Constitution mapping, substitute all placeholders
3. Value changes only modify the Constitution in one place; all templates auto-align

---

## Gate Three: Generate Five Documents

```
{project}/specs/{change_id}/
├── CONSTITUTION.md    ← Supreme authority
├── spec.md            ← What + Why + Acceptance
├── tasks.md           ← Task + Dependencies + Verification
├── checklist.md       ← DoD + Anti-Perfunctory + Scenario Regression
└── decisions.md       ← Decisions + Pitfalls + Audit Methodology
```

### Behavioral Hard Constraints

**1. No Placeholders During Generation**

Prohibited in spec/tasks/checklist:
- "TBD" / "TODO" / "to be added later" / "same as above"
- "Add appropriate error handling" (without specifying exactly how)
- "Write tests for the above" (without content or acceptance criteria)
- "Similar to Task N" (executor may read out of order)
- Describing what to do without showing how (code steps must include code/command blocks)
- Referencing types, functions, or methods not defined in any Task

**2. Bidirectional Links**

spec/tasks/checklist must have bidirectional references — one-way references prohibited:
```
spec.md:     "R3: Write rejection protection → tasks Task 5, checklist §3 R3-1/R3-2"
tasks.md:    "Task 5: Implement write rejection → spec R3, checklist §1.5"
checklist.md: "§1.5 Write rejection verification → spec Scenario R3-1, R3-2"
```

**3. Scenario Numbering System**

`R{requirement_number}-{sequence_number}`. checklist Part 3 must reference every Scenario:
```
spec R3 has 3 Scenarios: R3-1 (normal write), R3-2 (dedup), R3-3 (rejection)
→ checklist §3 must include all 3 with expected results
→ tasks Task 5 must cover R3-1 through R3-3
```

**4. Base Change Propagation**

decisions.md or Constitution changes → re-run this Gate → diff → update only affected sections → log changes.

---

### spec.md Structure

Declaratively define "what success looks like." Do not bind to execution paths.

**Required Sections:**

- **Why**: Rationale + current baseline with measured data
  ```
  Correct:   "faiss_doc_count=8494, write QPS≈15/s, 14 deps occupying 1.2GB; reducing to 10 frees 400MB"
  Wrong:     "Current data volume is large; performance needs improvement" (no numbers)
  ```

- **What Changes**: Added / Modified / Deprecated / Shared Infrastructure / Documentation Sync / BREAKING
  ```
  Correct:
  - Added: reranker.py (Rerank service wrapper, replaces sentence-transformers)
  - Modified: writer.py:write_batch() adds expiration marking logic
  - Deprecated: requirements.txt 14→10 packages (remove 4 unneeded)
  Wrong: "Optimize dependencies, refactor write" (no specific files)
  ```

- **Impact**: Affected + **Explicit No-Change** (Red Lines)
  ```
  Correct:   Affected: writer.py, requirements.txt, Dockerfile | No-Change: searcher.py, faiss index, torch
  Wrong:     "Affects write module" (no files, no no-change list)
  ```

- **Execution Constraints**: All constraints from source document, carried over exhaustively
  - **Pre-Check Counting**: Count source constraints (N) before generation. Count output constraints (M) after. N≠M → supplement and re-run.
  ```
  Correct:   Source has 5 constraints → spec carries over all 5, numbered ①~⑤
  Wrong:     Source has 5 → spec carries 3 + writes "others similar"
  ```

- **ADDED / MODIFIED / REMOVED Requirements**: Each with SHALL declaration + Scenario. REMOVED must exist (even if "None"), with removal reason + transition plan.

- **Rollback Mechanism**: Trigger condition + objective + mandatory 4-column table:
  ```
  | Step | Action | Command/Operation | Verification |
  |------|--------|-------------------|--------------|
  | 1    | Stop service | taskkill /F /PID xxx | All ports closed |
  | 2    | Restore data | xcopy .backup/xxx .data/ /E | File count matches |
  ```

**Self-Containment Rule**: Core data structures (schema), interface signatures, configuration fields, and error codes — if they exist — must be fully written in spec. Spec is the acceptance anchor. "See tasks.md" for these = fail.

**Format Rules**: Must include correct/counterexample pairs:
```
Format Rule: {rule description}
Correct: {specific value, real example}
Counterexample: ❌ {specific wrong value} → ✅ {correct form}
```

**Compound Constraints**: Must be expanded — "enforce verification rigorously" is 4 words of nothing:
```
Correct: "① Data format validation: check every required field in JSON schema exists with correct type
          ② Consistency verification: faiss_doc_count delta = records written this batch
          ③ Failure handling: rollback this batch + write error_log + return HTTP 503"
Wrong:   "Enforce verification rigorously"
         "Error handling" (zero specifics)
```

---

### Anti-Corner-Cutting Clause

This is the intellectual core of Super-Spec. The following keywords, when appearing in the skill, must be executed according to their operational definitions. Shrinking, omitting, or downgrading is prohibited.

**A. Semi-Structured Constraints (Most Frequently Shortcutted)**

| Keyword | Operational Definition | Common Shortcut | Check |
|---------|------------------------|-----------------|-------|
| **Exhaustive** | Carry over every item from source. Pre-Check: count source items (N) before, count output (M) after. N≠M = fail. | "Selectively carry over," "only key items," "others similar" | #4 |
| **Expand** | Every lock/step/phase must specify: ① what to check ② how to verify ③ what to do if it fails. Writing only the name is prohibited. | "Enforce verification rigorously" (4 words), "Error handling" (no specifics) | #3 |
| **At Least N** | N is the floor. "At least 5 rounds" = 5 minimum; must not shrink to 3. | "At least 5 rounds" → writes 3; "at least 1 exception test" → writes none | #11 |
| **Mandatory Template** | Template structure must be fully filled. Writing only the template name is prohibited. | "Use 4-column table" → writes plain text; "Attach examples" → writes "correct/incorrect format" | #2/#5 |
| **List All Items** | Source has N items → output must have all N, numbered and countable. | Writing ①②③, omitting ④; merging multiple items into one | #3/#4 |

**B. Content-Type Constraints (Models Replace Specifics with Abstractions)**

| Scenario | Operational Definition | Common Shortcut | Check |
|----------|------------------------|-----------------|-------|
| **Red Line List** | Per file/module. Vague "don't touch existing code" prohibited. | "Existing services untouched," "Core logic unchanged" | #12 |
| **Terminology** | Each term = one-sentence definition + cross-module mapping. Circular definitions prohibited. | "supersede is a versioned replacement mechanism" (no details on old version handling) | #12 |
| **Baseline Measurements** | Why section baseline data must include specific values. "N records," "mostly OK" prohibited. | "Large data volume," "Performance acceptable" | #12 |
| **Interface/Configuration** | Schema must be fully written. Interface signatures, config fields, error codes — if they exist, must be in spec. Exists but not written = fail. | Has schema, missing interface/config/error codes | #1/#13 |
| **Specific > Abstract** | "Verification coverage" → itemize "verify ①…②…③…". "Error handling" → specify what errors + how to handle. | "Lint verification," "Error handling," "Appropriate configuration" | #3 |

**C. Structural Constraints (Models Will Skip/Leak)**

| Scenario | Operational Definition | Common Shortcut | Check |
|----------|------------------------|-----------------|-------|
| **REMOVED Section** | Must exist (even if "None"). Each item: removal + reason + transition plan. | Skipping REMOVED entirely | #14 |
| **Risk Response** | decisions.md must include risk list: risk + severity + trigger phase + response + acceptance criteria. | Not listing, or "see spec" | #15 |
| **Execution Discipline** | tasks header must extract from Constitution principles item by item. Missing any = fail. | Writing 2-3 items, or "follow architecture principles" | #14 |
| **File Structure** | tasks must list File Structure before Tasks. Create/Modify/Test per file. | Skipping directly to writing Tasks | #14 |
| **Scenario Carry-Over** | checklist Part 3 must carry over every Scenario + expected result. IDs only = fail. | "R1-1~R1-5" (no expected results) | #9 |

**D. Output Integrity (Models Will Truncate/Leave Traces)**

| Scenario | Operational Definition | Common Shortcut | Check |
|----------|------------------------|-----------------|-------|
| **Anti-Truncation** | If file estimated >8000 words, P0 tail content (constraints/risks/rollback) must be moved forward. Truncation = generation failure. | Tail risk table/REMOVED truncated | #16 |
| **Remove AIGC Metadata** | Output must not contain AIGC metadata or "Generated by AI" footers. Grep each file and remove. | Retaining platform-injected AIGC markers | #16 |
| **Verification Without Self-Deception** | Checklist must be verified against actual output files (grep, line count, content inspection). Filling "Yes" without reading = prohibited. | 10 "Yes" answers in one second | #16 |
| **Cross-Document Consistency** | If spec says A, tasks/checklist/decisions cannot say B. Scenario IDs must be consistent. | spec R1 has 5 Scenarios; checklist only lists 3 | #9 |

---

### tasks.md Structure

**Header: Execution Discipline** — extracted from Constitution core principles. Vague "follow architecture principles" prohibited.

```
## Execution Discipline
1. Progressive Rule: R1 scan → R2 review → R3 root-cause → R4 verify → R5 final
2. Restart after code change: Any .py/.json change must restart service before verification
3. Verification ≠ Execution: Running tests ≠ functionally correct; must inspect logs + output
4. Main Thread Discipline: Write operations only on main thread; concurrent faiss writes prohibited
```

**Task Decomposition** — each Task includes sub-tasks + determinable verification criteria. After completion, must attach:
- **Evidence**: Script name + pass count / live e2e results (non-repudiable)
- **Key Patches**: Pitfalls encountered (optional)
- **Deviation on Record**: Target vs measured + acceptance rationale (optional)

**Task Decomposition Iron Rules:**
- **Destructive Operation → Pre-Flight Check**: First sub-task must be a pre-flight check:
  ```
  - [ ] {N}.0: Pre-Flight Check (before {operation}): {check 1} + {check 2} + ... ; halt if conditions not met
  ```
- **P0 Risk → Fallback Protection**: Must have fallback sub-task:
  ```
  - [ ] {N}.x: {Risk} fallback: {normal path} failure → {fallback action} ({why this cannot block upstream})
  ```
- **Cutover → Rollback Drill**: Must include rollback drill sub-task:
  ```
  - [ ] {N}.x: Rollback drill: execute spec rollback table step by step in dry mode; verify each step passes
  ```

**Footer**: Dependency graph.

---

### checklist.md Structure

**Part 1: DoD Quantitative Verification** — Instance template DoD + module-specific items. Each: "Yes/No + Evidence"

**Part 2: Anti-Perfunctory Self-Check**

| # | Trap | Defense |
|---|------|---------|
| 1 | Verification ≠ Execution | Acceptance items with "verify/confirm/test" must have execution evidence |
| 2 | Fix ≠ Verified Fix | After fix, restart + re-run that section's acceptance |
| 3 | All Green ≠ Truly Green | Final round: spot-check 3 ✅ items using different method |
| 4 | Context Break | Each round start: list previous key issues; each phase: re-read Constitution |
| 5 | Happy Path Bias | At least 1 abnormal input test per section |
| 6 | Fix Introduces New Issues | After modifying shared/ or interfaces, re-run integration tests immediately |
| 7 | Fallback Path Perfunctory | Each fallback/protection mechanism must have ≥1 trigger verification |
| 8 | Verification Perfunctory | "Item-by-item" = main thread personally reviews each item; batch/LLM/script bypass prohibited |

**Part 3: Scenario Regression** — Every spec Scenario carried over with expected results, grouped by R (R1/R2/R2.5/R3/R4/R5/R6 tables).

---

### decisions.md (Knowledge Base)

Consulted when ambiguity arises. Not involved in daily execution:
- **Confirmed Decision Table**: All Gate One conclusions
- **Known Pitfalls**: Pitfalls from actual testing
- **Risk Response List**: Each item = risk + severity (P0/P1) + trigger phase + response + acceptance criteria
  ```
  | Risk | Severity | Trigger Phase | Response | Acceptance Criteria |
  |------|----------|---------------|----------|---------------------|
  | faiss write concurrency | P0 | Phase 2 | Main thread serial + pre-write lock | 0 errors on concurrent write |
  | Dependency incompatibility | P1 | Phase 1 | Lock requirements.txt + CI verify | All imports successful |
  ```
- **Audit Methodology**: Three-perspective — Reviewer, Code Generator, Intent Alignment

---

### Gate Three Post-Generation Verification (18 Items)

Must actually read output files (grep, line count, content inspection). Filling "Yes" without reading = prohibited. Any "No" → patch and re-verify.

| # | Verification Item | Anchor | Result |
|---|-------------------|--------|--------|
| 1 | spec schema fully written; interface/config/error codes written if they exist; no "see tasks" | Interface/Config | Yes/No |
| 2 | Each format rule has specific correct/counterexample pair (not "correct/incorrect format") | Mandatory Template | Yes/No |
| 3 | Each compound constraint expanded (what to check + how to verify + what to do if fails) | Expand / List All / Specific | Yes/No |
| 4 | spec execution constraints exhaustively match source (count N, count M; N=M) | Exhaustive + Pre-Check | Yes/No |
| 5 | spec rollback mechanism is 4-column table (Step/Action/Command/Verification) | Mandatory Template | Yes/No |
| 6 | Each destructive operation Task has pre-flight check sub-task | — | Yes/No |
| 7 | Each P0 risk Task has fallback protection sub-task | — | Yes/No |
| 8 | Cutover phase has rollback drill sub-task | — | Yes/No |
| 9 | Bidirectional links complete + Scenario IDs consistent (spec R1 has 5 → checklist has 5) | Cross-Document + Scenario | Yes/No |
| 10 | No "No Placeholders" violations (no TBD/TODO/PENDING) | — | Yes/No |
| 11 | Progressive rule meets or exceeds source requirement ("at least 5" not shrunk to 3) | At Least N | Yes/No |
| 12 | Constitution red lines per file; each term has definition + mapping; spec Why baseline has specific values | Red Lines / Terms / Baseline | Yes/No |
| 13 | Each ADDED Requirement: interface/config/error codes fully written if they exist | Interface/Config | Yes/No |
| 14 | spec REMOVED section explicitly present; tasks has File Structure + execution discipline from Constitution | REMOVED / Discipline / Structure | Yes/No |
| 15 | decisions.md has risk response list (risk + severity + trigger phase + response + acceptance) | Risk Response | Yes/No |
| 16 | Grep: no AIGC metadata/footer; spec not truncated (tail sections complete) | Remove AIGC / Anti-Truncation | Yes/No |
| 17 | checklist anti-perfunctory covers fallback verification (each fallback has ≥1 trigger test) | #7 Fallback | Yes/No |
| 18 | "Item-by-item" verification: main thread personally reviewed (no batch/LLM/script bypass) | #8 Verification | Yes/No |

---

## Gate Four: Progressive Execution

After user approval:
1. Advance per tasks.md. After each section: clean temp files → log changes → update progress
2. Output independent summary per section/phase (≥3 lines)
3. **Re-read Constitution first 3 sections before each round** (principles + decisions + red lines) to prevent drift
4. After completing each Task, check off and attach evidence + patches + deviations
5. New decision points mid-way → pause and return to Gate One; scope expansion without authorization prohibited
6. All P0 green before entering next round

---

## Gate Five: DoD Final Verification

Execute checklist.md all three parts item by item. Record "Yes/No + Evidence" for each. Any "No" → return to Gate Four, fix, re-verify. Final verification uses Constitution as supreme authority.

---

## Gate Six: Wrap-Up

- [ ] Cold start normal
- [ ] 5-minute health check stable
- [ ] Token/version number consistent
- [ ] Key closed loops pass
- [ ] Fallback behavior correct
- [ ] Performance baseline has data
- [ ] Cleanup verified
- [ ] Change log complete
- [ ] Documentation sync consistent
- [ ] Constitution archived
- [ ] Five-document bidirectional links complete
- [ ] Output final report

---

## Degradation and Exceptions

- Template missing → error and stop; reconstruction from memory prohibited
- User abort → retain artifacts + progress; do not delete
- Context break → resume from progress table at most recent phase
- Constitution missing → complete first, then proceed
- decisions vs execution conflict → decisions + Constitution take precedence; regenerate affected documents

---

## Constitution Maintenance

| Trigger | Action |
|---------|--------|
| Decision change | Update confirmed decisions section; annotate date + reason |
| New red line | Append + explain why |
| New terminology ambiguity | Append to terminology table |
| Placeholder value change | Update mapping; templates auto-align |
| Phase/round start | Re-read Constitution first 3 sections |
| DoD final verification | Verify against every Constitution item |

---

## Solo Developer Optimization

Traditional spec frameworks assume teams — code review, PR processes, people to backstop failures. Solo developers + AI have none of these. A mistake becomes a production incident.

| Team Assumption | Solo + AI Reality | Super-Spec Response |
|-----------------|-------------------|---------------------|
| Implementers read specs carefully | AI "intelligently" bypasses rules | 4 categories of anti-corner-cutting + 18-item checklist |
| Someone reviews quality | One person and AI | Five-document interlocking substitutes team review |
| Memory/context reliable | Long conversations drift; cross-session loss | Constitution re-read every round; no reliance on memory |
| Environment stable | Frequent machine/port/dependency changes | Probe-driven; zero hard-coding |
| "Looks fine" can pass | No one to backstop | Evidence-based + spot-check re-verification |
| Spec is referenced | Spec is forgotten | Gates Three → Five → Six continuously anchor to spec |

---

## Reference Patterns

The following are validated practices from real projects. Not mandatory — proven approaches worth knowing.

### Progressive Rhythm

| Round | Cadence | Intent |
|-------|---------|--------|
| R1 | Scan — find all issues; fix P0 blockers | Establish problem landscape |
| R2 | Review — did R1 fixes introduce new issues + missed edges | Prevent fix-induced bugs |
| R3 | Root-Cause — check if similar issues exist elsewhere; fix systemically | Systematic, not whack-a-mole |
| R4 | Verify — did first three rounds introduce new bugs | Second-order verification |
| R5 | Final — spot-check 3 ✅ items via different method | Anti-perfunctory |

Small projects: ≥3 rounds. Large: ≥5, potentially 7-10+.

### Phase Division

1. **Environment Check + Baseline** → Baseline data complete and reproducible
2. **Per-Service Audit** → P0 count confirmed no omissions
3. **Integration Verification** → Core links no breakpoints
4. **Centralized Fix** → Issues cleared + trigger-based prevention
5. **Boundary + Security** → All boundaries pass + no high-risk security issues
6. **Cleanup + Stress Test + Wrap-Up** → Performance meets targets + no leaks + docs consistent

Small projects can merge 2-4 into one "audit + fix + verify" round.

### Task Decomposition Example

Good — each Task follows file boundaries; determinable in 2-5 minutes:
```markdown
- [ ] Task 3: Implement data_writer.py (depends on Task 1)
  - [ ] 3.1: write_record() basic write + dedup check
  - [ ] 3.2: Version chain append + expiration marking
  - [ ] 3.3: Input validation + reject illegal data
  - Verification: test_data_writer.py 42/42 PASS
```

Poor — too vague:
```markdown
- [ ] Task 3: Complete all data_writer functionality
  - Verification: tests pass
```

### File Structure

Lock file boundaries before writing Tasks:
```markdown
## File Structure
- Create: `service/matcher.py` — Match scheduling logic
- Create: `service/calibrator.py` — Calibration learner
- Modify: `core/server.py:845-920` — Write gateway → data_writer
- Modify: `requirements.txt` — 12→8 (dependency reduction)
- Test: `tests/test_data_writer.py` — CRUD + version chain + validation
```

### Evidence Attachment

```markdown
- [x] SubTask 3.1: write_record() basic write + dedup
  - Evidence: test_data_writer.py 42/42 PASS; live e2e ALL PASS
  - Key Patches: ① record_id key name compatibility fix ② concurrent write path isolation
  - Deviation on Record: Target ≤200ms, actual ~350ms; accepted per ≥10x degradation rule
```

### Scenario Coverage Dimensions

Per Requirement, select as needed: happy path / fallback failure / boundary value / concurrency safety / authentication / data migration / idempotency / observability.

P0: at least happy path + one boundary + one failure. P2: happy path + one boundary.

### Progress Tracking

Matrix (fill immediately after each section):
```
Round   Phase 0   Phase 1   Phase 1.5  ...   Phase N
R1      [ ]       [ ]       [ ]        ...   [ ]
R2      [ ]       [ ]       [ ]        ...   [ ]
```

Status: ✅ Passed / 🔧 Fixed / ⚠️ Open Issue / ❌ Not Passed / ⏭️ N/A (note reason)

Progress log (daily append): Completed / In Progress / Next / Blockers
