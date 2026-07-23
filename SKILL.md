---
name: "super-spec"
description: "Seven Gates from requirement lock to delivery—anti-laziness interception × five-document cross-validation × probe-driven, ensuring AI can't skip steps or pass empty"
license: MIT
---

# Super-Spec

## Security Declaration

| Dimension | Status |
|-----------|--------|
| Asset Type | Documentation-only |
| Network Requests | None |
| System Commands | None |
| File Deletion | Workspace only |
| External Dependencies | None |
| Data Collection | None |
| Security Level | Safe |

**Make AI walk through seven gates before delivery—not just spit out answers.**

Not a prompt, not a template. A complete engineering discipline system. Helps agents truly complete every step and produce verifiable deliverables, so users get **verified production-grade results**, not "looks fine."

---

## Six Design Principles

1. **Constrain behavior, not capability**—Don't teach what models excel at (architecture selection, technical solutions); lock down what models tend to skip (expansion, completeness, evidence, bidirectional links) with structure
2. **Structure locks, not prompt blocks**—No matter how good the prompt, models can bypass it. Only checklists that grep files line-by-line, Scenario IDs unified across documents, and evidence that can't be denied truly lock it down
3. **Divide and interlock**—Five documents each own one responsibility yet cross-validate: if spec says A, tasks can't say B. Drift has nowhere to hide
4. **Constitution-driven, not memory-driven**—Consistency doesn't rely on "what the model remembers" but on the Constitution **document being there in writing**
5. **Probe-driven, not hardcoded**—Ports/paths/dependencies/redlines are all probed and read in; zero changes needed when switching environments
6. **Evidence-based verification, not trust-based**—"Looks fine" doesn't count as passing. Final round spot-checks 3 OK items with a different verification method

### How Models Bypass Rules (This Is Why Structure Matters)

| You Say | It Does |
|---------|---------|
| "Enforce verification strictly" | 4 words done |
| "Full coverage required" | Skips 3 items, writes "others similar" |
| "Provide test evidence" | "Tests passed" with zero evidence |
| "Don't hardcode" | Hardcodes paths pretending otherwise |

---

## The Seven Gates Pipeline

```
Request → Gate 0·Anchor Review → Gate 1·Decision Points → Gate 2·Constitution → Gate 3·Five Documents → Gate 4·Progressive Execution → Gate 5·DoD Final Verification → Gate 6·Cleanup → Delivery
```

| Gate | What It Blocks | Pass Condition |
|------|---------------|----------------|
| 0·Anchor Review | Acting without understanding the current state | Current code facts + finalized decisions + no-change list, user confirmed |
| 1·Decision Points | Model filling in defaults on its own | Unresolved items NOT defaulted; ask user one by one |
| 2·Constitution | Understanding drift every time | Constitution 7 sections locked; five documents implicitly inherit |
| 3·Five Documents | Laziness / skipping / passing empty | Anti-laziness clauses + 10-item verification checklist as dual safety net |
| 4·Progressive Execution | Declaring done in one round | ≥3 progressive rounds; all Must items green before advancing |
| 5·DoD Final Verification | Self-deceptive verification | Evidence item by item + spot-check 3 OKs with alternate method |
| 6·Cleanup | Omissions / garbage left behind | 12-item cleanup checklist verified item by item |

**Not "recommended to complete"—it's "can't deliver without completing."**

## Five Documents Interlock

```
CONSTITUTION.md  ← Supreme authority, drives everything
   ↓ implicit inheritance
spec.md          ← What + Why + Scenario
   ↔ bidirectional links
tasks.md         ← How + Dependencies + Evidence
   ↔ bidirectional links
checklist.md     ← Verify + DoD + Anti-going-through-motions
   ↕ ambiguity fallback
decisions.md     ← Decisions + Pitfalls + Risk responses
```

After division: cross-validate—inter-document consistency, Scenario completeness, bidirectional links prevent tunnel vision, base changes trigger diff updates.

---

## Optimizations for Individual Users

Traditional spec frameworks are designed for teams—with code review, PR processes, and people to backstop. Individual users + AI have none of these; mistakes become production incidents.

Super-Spec addresses this reality with key optimizations:

| Team Spec Assumptions | Individual + AI Reality | Our Response |
|----------------------|------------------------|--------------|
| Implementers will read the spec carefully | AI will "cleverly" bypass rules | 4 types of anti-laziness detection + 10-item verification checklist |
| Someone reviews quality | Just one person and AI | Five-document interlock replaces team cross-verification |
| Memory/context is reliable | Long-conversation drift, cross-session loss | Constitution re-read every round, not memory-dependent |
| Environment is stable and uniform | Frequent computer changes, port changes, dependency upgrades | Probe-driven, zero hardcoding |
| "Looks fine" can pass | No one to backstop if something goes wrong | Evidence verification + spot-check re-verification |
| Spec written, then referenced | Spec written, then forgotten | Gates 3→5→6 anchored to spec throughout |

**Core philosophy**: No team review? Use structural review. Turn what teams do into document interlocking and verification checklists done automatically.

## Escape Hatch: Gate Determination

Not all seven gates are required every time. **Auto-determined by task risk level:**

| Level | Condition | Gates to Walk |
|-------|-----------|---------------|
| Light | Small task / low risk / user has given precise instructions | 0·Anchor → 2·Constitution (lite) → Delivery |
| Standard | Medium complexity / has dependencies / multi-file changes | 0→1→2→3→4→5→6 (full pipeline) |
| Heavy | New project / core module / major version upgrade / high risk | Full pipeline + ≥3 rounds per stage + rollback drill |

**Determination rules:**
- Changes < 3 files, no new dependencies, no breaking changes → Light
- Changes 3-10 files, new dependencies or data migration → Standard
- Changes > 10 files, core architecture changes, user requests "follow Spec discipline" → Heavy

**Skipping gates ≠ skipping anti-laziness.** Even Light level, the streamlined verification checklist (10 items) from Gate 3 must pass.

## Trigger Conditions

- New project / new core module / new service / major version upgrade / user requests "follow Spec discipline"

## Prerequisites

Before invoking this skill, **at least one** of the following inputs must already exist (or a combination):

- Complete design document (architecture design / tech selection / upgrade roadmap, etc.)
- Requirements document (functional requirements / acceptance criteria / constraints, etc.)
- Development document (API design / data models / interface specs, etc.)
- Prompt document (agent behavior rules / execution discipline / output format, etc.)

This skill **does not create requirements out of thin air**—it transforms existing design documents into a structured five-document system (Constitution/spec/tasks/checklist/decisions), handed to the agent for disciplined execution through the gates.

## Iron Rules (Violation = Rerun)

| # | Rule | Why It's Iron (Behavioral) | Violation Example |
|---|------|---------------------------|-------------------|
| 1 | Read template before generating documents → Redo | Model skips reading template, generates directly | Writing spec without reading Constitution template |
| 2 | Unresolved decision points MUST NOT be defaulted → Ask | Model fills in defaults on its own | "Default to SQLite" (didn't ask user) |
| 3 | NO chapter merging—each chapter outputs independent summary | Model merges to save effort | "Gates 3, 4, 5 merged output" |
| 4 | NO skipping chapters | Model skips "unimportant" chapters | Skipping Impact analysis, writing Task directly |
| 5 | NO passing empty—must provide execution evidence | Model says "looks fine" | Checklist all "Yes" with no evidence attached |
| 6 | Each chapter complete: clean temp files → log changes → update progress | Model skips cleanup steps | Ran but didn't log changes; next round doesn't know what changed |
| 7 | ❌ or unfilled items from previous round → CANNOT enter next round | Model pushes forward with wounds | R1 has 2 ❌ but directly enters R2 |
| 8 | Fix obstacles immediately, no leftover tails | Model marks "handle later" to bypass | "TODO: test in production" |
| 9 | Respect template redlines (dynamic paths / single Token source / no silent logs, etc.) | Model hardcodes, fails silently | Hardcoding `/home/user/` paths |

---

## Gate 0: Anchor Review

After receiving requirements—**first step**: understand the current state before discussing design. Output an "Anchor Checklist":

1. **Current Code Facts**: Existing utility functions / data structures / API parameters / auto-update chains, list each with location + design impact
2. **Finalized Historical Decisions**: From project memory / historical Specs / things user previously said
3. **Explicit No-Change List**: Modules/files/logic that will NOT be touched this round

After user confirmation, proceed to Gate 1.

## Gate 3: Generate Five Documents

After Constitution is confirmed, generate using the **five-document division**:

```
{project}/specs/{change_id}/
├── CONSTITUTION.md    ← Supreme authority
├── spec.md            ← Acceptance layer: What + Why + Acceptance
├── tasks.md           ← Execution layer: Task + Dependencies + Verification
├── checklist.md       ← Anchor layer: DoD + Anti-going-through-motions + Scenario regression
└── decisions.md       ← Knowledge base: Decisions + Pitfalls + Audit methodology
```

**Relationships**: Constitution drives spec/tasks/checklist generation; decisions is the knowledge base, consulted on ambiguity. Base changes → rerun this gate → diff update.

### Behavioral Hard Constraints

**1. No Placeholders (Anti-Laziness at Generation Time)**

The following patterns are **forbidden** in spec/tasks/checklist:
- "TBD" / "TODO" / "pending" / "supplement later" / "same as above"
- "Add appropriate error handling" (without specifying how)
- "Write tests for the above" (without concrete content or judgment criteria)
- "Similar to Task N" (executor may read out of order)
- Describing what to do without showing how (code steps must include code/command blocks)
- Referencing types/functions/methods not defined in any Task

**2. Bidirectional Links (Anti-Tunnel-Vision)**

spec/tasks/checklist must have bidirectional references:
- spec.md: each Requirement → `tasks.md Task N, checklist section 3`
- tasks.md: each Task → `spec R{N}, checklist section 1.{item}`
- checklist.md: each item → `spec Scenario R{N}-{M}`

Unidirectional links forbidden (spec→tasks exists but tasks→spec doesn't).

**3. Scenario Numbering System (Structural—Without Numbers, Cross-Document Reference Is Broken)**

`R{requirement#}-{sequence#}`, e.g., R1-1, R1-2, R3-1, R5-3. Checklist Part 3 directly references these.

**4. Base Change Propagation (Anti-Drift)**

decisions.md or Constitution changes → rerun this gate → diff comparison → update only affected sections → log changes

### Pitfall Alerts (Write broad, don't hardcode—pitfall examples are illustrative, not hard constraints)

| Pitfall | Alert | Example (illustrative, not exhaustive) |
|---------|-------|---------------------------------------|
| File Structure | Lock file boundaries before writing Tasks, otherwise new files keep appearing later | After 5 Tasks discover a 6th file needs changing, must retro-edit all Tasks |
| Attached Evidence | Only checkmarks without evidence = self-talk; next person modifying code won't trust it | "Verification passed" vs "test_xxx.py 42/42 PASS" |
| Post-Generation Self-Check | Not looking back at spec coverage after generation, often misses requirements | Tasks written but spec R5 has zero Task coverage |
| Phase Self-Check | Running everything then checking at the end; mid-course deviation costs heavily | R3 went off-direction, R5 discovered it, 2 rounds wasted |
| Spec Length | Cut design narrative, keep only What+Why+Scenario, but self-contained rule prevails—rather be long than write "see tasks.md" | "Config details see tasks Task 3" → implementer must jump to know config items |

### spec.md Structure

Declaratively defines "what success looks like," doesn't bind to execution path.

**Required Sections:**

- **Why**: Why we're doing this + current baseline measured data
- **What Changes**: Added / Modified / Deprecated / Shared infrastructure / Documentation sync / BREAKING
- **Impact**: Affected + **Explicit No-Change** (redlines)
- **Execution Constraints**: ALL execution constraints from source documents **fully** copied over, checked item by item, no omissions
  - **Pre-check Count**: Before generation, count how many execution constraints the source has (N); after generation, count how many you wrote (M); if N≠M, fill in and rerun
- **DELTA SPECS (Incremental specs—ADDED / MODIFIED / REMOVED)**: Don't directly overwrite main spec; describe changes incrementally. Each contains SHALL declaration + Scenario + MoSCoW priority. REMOVED must exist (even if writing "none"), contains removal + Reason + transition plan. Priority: **Must** (this round required) / **Should** (this round try) / **Could** (optional) / **Won't** (explicitly not doing)
- **Rollback Mechanism**: Trigger conditions + target + steps table (mandatory 4-column template)

**spec Self-Containment Rule (Anti-"see tasks.md" Trap):**
- Core data structures must be fully written within spec
- Format rules must include positive/negative examples
- Compound constraints must be expanded

### Anti-Laziness Clauses (Model Laziness Complete Map + Hard Landing)

The following keywords/scenarios appearing in the skill MUST execute per their operational definition; shrinking, omitting, or downgrading is forbidden:

**A. Semi-Structural Constraints (Most Frequently Skimped)**

| Keyword | Operational Definition | Common Laziness Tactic | Check |
|---------|----------------------|----------------------|-------|
| **Full** | Source has N items → output N items, checked one by one, no omissions | "Selectively include" "Only key items" "Others similar" | #4 |
| **Expand** | Each lock/step/phase must specify: ①what to check ②how to verify ③what if it fails | "Enforce verification strictly" (4 words only) | #3 |
| **At least N** | N is the floor, not the default | "At least 5 rounds" → actually writes 3 | #11 |
| **Mandatory template** | Template structure must be fully filled out | "Use 4-column table" → writes plain text | #2/#5 |
| **List all** | Source has N constraints/locks/rules → output must have N, numbered and countable | Only writes ①②③, misses ④ | #3/#4 |

**B. Content-Type Constraints (Model Replaces Specific with Abstract/Vague)**

| Scenario | Operational Definition | Common Laziness Tactic | Check |
|----------|----------------------|----------------------|-------|
| **Redline List** | List per file/per module; "existing code unchanged" vague language forbidden | "Existing services unchanged" "Core logic unchanged" | #12 |
| **Term Definitions** | Each term = one-sentence definition + cross-module mapping; circular definitions forbidden | "supersede is a versioned replacement mechanism" | #12 |
| **Baseline Measurement** | Why section baseline data must state concrete values/status | "Has lots of data" "Performance acceptable" | #12 |
| **Interface/Config** | Schema must be fully written; if interface signatures/config fields/error codes exist, must be fully written in spec | Only has schema, missing interface/config/error codes | #1/#13 |
| **Concrete > Abstract** | "Verification coverage" → expand to "Verify ①…②…③…" listed item by item | "Lint check" "Error handling" "Appropriate config" | #3 |

**C. Structural Constraints (Model Skips or Misses)**

| Scenario | Operational Definition | Common Laziness Tactic | Check |
|----------|----------------------|----------------------|-------|
| **REMOVED section** | MODIFIED/REMOVED must both exist; REMOVED must be explicit even if "none" | Skips REMOVED section | #14 |
| **Risk Response** | decisions.md must include risk response checklist | Not listed or "see spec" | #15 |
| **Execution Discipline** | tasks opening execution discipline must extract from Constitution core architecture principles, listed item by item | Only 2-3 items or vague "follow architecture principles" | #14 |
| **File Structure** | tasks must first list File Structure before writing Tasks | Skips directly to Task writing | #14 |
| **Scenario Completeness** | checklist Part 3 must copy every Scenario from spec + expected results | "R1-1~R1-5" (no expected results) | #9 |

**D. Output Integrity (Model Truncates or Leaves Traces)**

| Scenario | Operational Definition | Common Laziness Tactic | Check |
|----------|----------------------|----------------------|-------|
| **Anti-Truncation** | If single file estimated >8000 words, Must-priority content at spec tail must be moved forward | Spec tail risk table truncated and lost | #16 |
| **Clean AIGC** | Output must NOT contain AIGC metadata or "AI-generated" footer | Keep platform-injected AIGC markers | #16 |
| **Verification Not Self-Deceptive** | Post-generation checklist must actually check item by item; forbidden to fill "Yes" without reading files | 10 "Yes" filled in 1 second | #16 |
| **Cross-Document Consistency** | If spec says A, tasks/checklist/decisions cannot say B | spec R1 has 5 items, checklist only lists 3 | #9 |

**Core Principle**: Structural rules ≈ 0 gap; **semi-structural and content-type are laziness hotspots**, must be locked down with operational definitions.

Requirements annotated with MoSCoW priority: **Must** (this round required, no delivery without passing) / **Should** (this round try to implement) / **Could** (this round optional) / **Won't** (explicitly not doing). Must items must all be green this round.

### tasks.md Structure

**Opening: Execution Discipline** (Extracted from Constitution core architecture principles, centralized, not scattered)

**Task Breakdown:** Each Task contains sub-tasks + determinable verification criteria. Upon completion, **must attach**:
- **Evidence**: Script name + pass count / live e2e results
- **Key Fixes**: Pitfall log (optional)
- **Deviation on Record**: Target vs measured + acceptance rationale (optional)

**Task Breakdown Iron Rules:**
- **Destructive operations → pre-checks**
- **Must-level risk → degradation protection**
- **cutover → rollback drill**

**End: Dependency Graph**

### checklist.md Structure

**Part 1: DoD Quantified Verification**—Each item "Yes/No + Evidence"

**Part 2: Anti-Going-Through-Motions Self-Check**

| # | Trap | Defense | Check |
|---|------|---------|-------|
| 1 | Verification ≠ Execution | Any acceptance containing "verify/confirm/test" must have execution evidence | |
| 2 | Fix ≠ Verify the fix | After fix: restart + rerun that chapter's acceptance | |
| 3 | All-green ≠ Truly green | Final round spot-check 3 checkmarks with alternate method | |
| 4 | Context break | Each round start: list previous round key issues; each phase: re-read Constitution | |
| 5 | Happy Path bias | At least 1 abnormal input test per chapter | |
| 6 | Fix introduces new problems | After modifying shared/ or interfaces: immediately rerun integration tests | |
| 7 | Degradation path going through motions | Each degradation/protection mechanism: at least 1 trigger verification | |
| 8 | Verification going through motions | "Item by item" "one by one" verification items: main thread personally audits | |

**Part 3: Scenario Regression**—Every Scenario from spec.md, grouped by R, copied over + expected results

### decisions.md (Knowledge Base)

Not involved in daily execution; consulted on ambiguity:
- **Decision Table**: All Gate 1 conclusions
- **Known Pitfalls**: Pits actually encountered
- **Risk Response Checklist**: Each item: risk + level + trigger phase + response + acceptance criteria
- **Audit Methodology**: Reviewer (BZ) / Code Generator (GZ) / Intent Alignment (MZ) three perspectives

### Gate 3 Post-Generation Verification (Anti-Model-Omission + Anti-Laziness)

After five documents are generated, verify the following checklist item by item. **Must actually read the generated files to verify.** Any "No" → fix and re-verify until all green before delivering to user:

| # | Verification Item | Original Check Points | Judgment |
|---|-------------------|----------------------|----------|
| 1 | **spec Completeness**: schema/interface signatures/config fields/error codes (if any) fully written + format rules include concrete positive/negative examples (not useless examples) | 1,2,13 | Yes/No |
| 2 | **Execution Constraints Full + Expanded**: Execution constraints fully consistent with source (N=M checked item by item) + compound constraints expanded item by item (what to check / how to verify / what if fails) | 3,4 | Yes/No |
| 3 | **Rollback Mechanism**: 4-column table (step/action/command/verify), not plain text | 5 | Yes/No |
| 4 | **tasks Safety Net**: Destructive operations → pre-checks + Must-level risks → degradation protection + cutover → rollback drill, all three required | 6,7,8 | Yes/No |
| 5 | **Cross-Document Consistency**: Five documents bidirectional links complete + Scenario IDs unified (spec has N Scenarios → checklist must have same count) | 9 | Yes/No |
| 6 | **No Placeholders**: No TBD/TODO/pending/supplement later/same as above/appropriate/on-demand | 10 | Yes/No |
| 7 | **Progressive Rule**: tasks progressive rounds ≥ source requirement + Must-class Requirements all covered | 11 | Yes/No |
| 8 | **Constitution Quality**: Redlines listed per file (not vague) + each term has definition+mapping (not circular) + spec Why has concrete baseline values | 12 | Yes/No |
| 9 | **Structural Completeness**: REMOVED section explicitly exists (includes removal/reason/transition) + tasks has File Structure + execution discipline fully extracted from Constitution + decisions has risk response checklist | 14,15 | Yes/No |
| 10 | **Output Trustworthy**: No AIGC metadata/footer residue + spec not truncated + degradation paths verified + "item by item" checks personally audited by main thread | 16,17,18 | Yes/No |

---

## Gate 4: Progressive Execution

After user approval, enter implementation:
1. Advance per tasks.md; each chapter complete: clean temp files → log changes → update progress
2. Each chapter/phase outputs independent summary (≥3 lines)
3. **Before each round starts, re-read Constitution first 3 sections** to prevent drift
4. Each completed Task: check off + attach evidence + fixes + deviations
5. Mid-course new decision points → stop and return to Gate 1; no self-expanding scope
6. All Must items green before advancing to next round

---

## Gate 5: DoD Final Verification

Execute all three parts of checklist.md item by item; each records "Yes/No + Evidence". Any "No" → return to Gate 4, fix and re-verify. Final verification uses Constitution as supreme criterion.

---

## Gate 6: Cleanup

- [ ] Cold start normal
- [ ] 5-minute health check stable
- [ ] Token/version numbers consistent
- [ ] Key closed loops passed
- [ ] Degradation behavior correct
- [ ] Performance baseline has data
- [ ] Garbage cleanup verified
- [ ] Change log no omissions
- [ ] Documentation sync consistent
- [ ] Constitution archived
- [ ] Five documents bidirectional links complete
- [ ] Output final report

## Degradation & Exceptions

- Template missing → Error and stop; no reconstructing from memory
- User abort → Preserve artifacts + progress; no deletion
- Context break → Resume from progress table at most recent phase
- Constitution missing → Fill in first before proceeding
- decisions conflicts with execution layer → defer to decisions + Constitution, regenerate affected documents

---

## Constitution Maintenance Obligations

| Trigger | Action |
|---------|--------|
| Decision change | Update finalized decisions section, annotate date + reason |
| New redline | Append + explain why |
| New term ambiguity | Append to glossary |
| Placeholder value change | Update mapping; templates auto-align |
| Phase/round start | Re-read Constitution first 3 sections |
| DoD final verification | Check every Constitution item one by one |

---

## References & Demonstrations (Capability Guidance—Not Constraints but Inspiration)

The following are verified good practices for reference and creativity. **Not mandatory—just proven useful approaches.**

### Progressive Mode Reference

| Round | Rhythm | Intent |
|-------|--------|--------|
| R1 | Sweep—find all issues, fix Must blockers first | Build problem landscape |
| R2 | Review—did R1 fixes introduce new problems + missed edges | Prevent fixing-introducing-new-bugs |
| R3 | Root-fix—do similar issues exist elsewhere; fix systematically | Systemic, not whack-a-mole |
| R4 | Verify—did previous 3 rounds of fixes introduce new bugs | Second-order verification |
| R5 | Final—spot-check 3 checkmarks with alternate method | Anti-going-through-motions |

Small projects: at least 3 rounds. Large projects: at least 5 rounds, potentially 7 or 10+. **Core: don't declare done in one round.**

### Phase Breakdown Reference

1. **Environment Check + Baseline** → Baseline data complete and reproducible
2. **Per-Service Audit** → Must-level issue count confirmed no omissions
3. **Integration Verification** → Core paths no breaks
4. **Centralized Fix** → Issues cleared + trigger-based prevention
5. **Boundary + Security** → All boundary values passed + security no high-risk
6. **Cleanup + Stress Test + Wrap-up** → Performance meets targets + no leaks + docs consistent

### Task Split Demonstration

Good splitting—each Task runs along file boundaries, determinable in 2-5 minutes:

```markdown
- [ ] Task 3: Implement data_writer.py write module (depends on Task 1)
  - [ ] 3.1: write_record() basic write + dedup check
  - [ ] 3.2: Version chain append + expiration marking logic
  - [ ] 3.3: Input validation + reject illegal data
  - Verify: test_data_writer.py 42/42 PASS
```

### Scenario Coverage Dimensions + EARS Format

**EARS Format (Recommended)**: `When <trigger>, the <system> shall <response>`

```
Good: "When user submits duplicate LRN, the brain_store shall return 409 error and reject the write"
Bad: "Duplicate writes should error" (missing trigger condition and system response)
```

Coverage dimensions: Happy Path / Degradation Failure / Boundary Values / Concurrency Safety / Auth & AuthZ / Data Migration / Idempotency / Observability

Must-level requirements: at minimum cover happy path + one boundary + one failure. Could-level requirements: at minimum happy path + one boundary.

### Progress Tracking Reference

Status: Passed / Fixed / Has Residual / Failed / N/A (note reason)

### Evidence Attachment Demonstration

```markdown
- [x] SubTask 3.1: write_record() basic write + dedup
  - Evidence: test_data_writer.py 42/42 PASS; live e2e ALL PASS
  - Key Fixes: (1) record_id key name compatibility fix (2) concurrent write path isolation
  - Deviation on Record: target <=200ms, measured ~350ms; accepted per >=10x significant degradation rule
```
