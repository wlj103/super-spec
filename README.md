# Super-Spec: Seven-Gate Engineering Discipline for AI Agents

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Standard: Agent Skills](https://img.shields.io/badge/Standard-Agent%20Skills-6e3ef7.svg)](https://agentskills.io)
[![Platform: Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-orange.svg)](https://claude.ai)
[![Platform: Cursor](https://img.shields.io/badge/Cursor-Compatible-000.svg)](https://cursor.com)
[![Platform: Codex](https://img.shields.io/badge/OpenAI%20Codex-Compatible-74aa9c.svg)](https://openai.com)


> 🛡️ **个人开发者神器** — 防AI偷懒、防AI作弊、防AI跳步。七道闸门 + 五文档互锁，让 AI 写代码时必须走完每一步，拿出证据，否则不准交差。
**A spec-driven development discipline for AI coding agents. Seven verification gates + five-document interlocking system prevent corner-cutting. Production-grade quality gates for Claude Code, Cursor, Codex, Copilot, Windsurf. Built for solo developers who need team-level engineering rigor.**

```
  REQUIREMENTS → G0:ANCHOR → G1:DECIDE → G2:CONSTITUTION → G3:5-DOCS → G4:EXECUTE → G5:VERIFY → G6:WRAP → DELIVERY
       ↓            ↓           ↓             ↓               ↓            ↓            ↓          ↓
  Source doc   Code facts   Decisions     Supreme law    Interlocking   ≥3 rounds    Evidence   12-item
  + PRD        + no-change  + rationale   + red lines    specs+tasks    all P0       + spot-    checklist
               list         + user asked  + constraints  +checklist     green        check
```

## Table of Contents

- [The Problem](#the-problem)
- [What Makes This Different](#what-makes-this-different)
- [Quick Start](#quick-start)
- [How It Works](#how-it-works)
  - [The Seven Gates](#the-seven-gates)
  - [The Five-Document Interlocking System](#the-five-document-interlocking-system)
  - [The Anti-Corner-Cutting Clause](#the-anti-corner-cutting-clause)
- [Architecture](#architecture)
- [Design Principles](#design-principles)
- [Who This Is For](#who-this-is-for)
- [Compared to Similar Tools](#compared-to-similar-tools)
- [Why "Super-Spec"?](#why-super-spec)
- [Real-World Impact](#real-world-impact)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

- [Key Features — What Makes This Unique](#key-features--what-makes-this-unique--核心功能--别人没有的)
## The Problem

AI coding agents are technically brilliant but behaviorally undisciplined. They **skip steps**, **fill in defaults without asking**, **claim "tests passed" with zero evidence**, and deliver results that "look fine" but break in production.

Prompt engineering doesn't fix this. Models learn to circumvent prompts — "enforce verification rigorously" becomes four words in the output: "Verification enforced rigorously."

**Super-Spec is not a prompt. It's a structural enforcement system.**

## Key Features — What Makes This Unique / 核心功能 — 别人没有的

Super-Spec is the only agent skill that **systematically catalogs how AI models cut corners** and creates **operational definitions** to prevent each tactic.

Super-Spec 是唯一一个系统性地**分类模型如何偷懒**、并为每种偷懒手段创建**操作定义**来阻止的 Agent Skill。

| Feature 功能 | Why It Matters 为什么重要 | High-Search Keywords 高频搜索词 |
|---------|---------------|------------------------|
| **Anti-Corner-Cutting Clause 反偷懒条款** | 4 categories of model shortcutting, each with operational definitions | stop AI skipping steps, prevent AI cutting corners, 防AI偷懒, 防AI作弊 |
| **Five-Document Interlocking 五文档互锁** | Constitution + spec + tasks + checklist + decisions cross-validate; spec says A, tasks cannot say B | cross-document verification, interlocking specs, 文档互锁, 规格验证 |
| **Constitution-Driven 宪法驱动** | Re-read Constitution every round; zero reliance on "the model remembers" | AI agent constitution, process discipline, AI流程纪律 |
| **Evidence-Based Verification 证据验证** | Script name + pass count + live e2e results required. "Tests passed" is not evidence | evidence-based AI, non-repudiable proof, AI验证证据 |
| **Solo Dev Optimized 个人开发者神器** | Five-document interlocking substitutes team review; no reviewer, QA, or PM needed | solo developer AI tools, 个人开发者神器, 单人团队级质量 |
| **Structural Locks 结构锁** | Grep-able checklists, Scenario IDs, 18-item checklist — prompts can be bypassed, structure cannot | structural verification, grep-able gates, 结构锁, 防绕过 |
| **Spot-Check Re-Verification 抽查复验** | Final round: pick 3 ✅ items, verify via different method. Prevents self-deception | AI self-verification, spot-check, 防AI自欺, 抽查验证 |
| **Pre-Flight + Rollback 预检+回滚** | Destructive operations get pre-flight check + rollback drill before execution | safe AI deployment, rollback drill, 安全部署, 回滚演练 |
| **Progressive ≥3 Rounds 渐进式≥3轮** | Gate Four enforces minimum 3 rounds; all P0 green before proceeding | progressive iteration, multi-round verification, 渐进式执行, 多轮验证 |
| **Seven-Gate Pipeline 七道闸门** | G0:Anchor → G1:Decide → G2:Constitution → G3:5-Docs → G4:Execute → G5:Verify → G6:Wrap | verification gates, AI engineering discipline, 七道闸门, 工程纪律 |

## What Makes This Different
## What Makes This Different

| Other Spec Tools | Super-Spec |
|-----------------|------------|
| "Write a spec" | Seven gates the agent must pass through; no skipping |
| Trust the agent to follow instructions | **Anti-Corner-Cutting Clause**: structural locks with grep-able checklists, cross-document Scenario IDs, non-repudiable evidence |
| Agent declares "done" | Gate Five: DoD Final Verification with spot-check re-verification |
| "Tests passed" | Evidence required: script name + pass count + live e2e results |
| Human review as quality gate | **Five-document interlocking** substitutes team review for solo developers |

Super-Spec is the only skill in the ecosystem that **systematically catalogs how models cut corners** and creates **operational definitions** to prevent each tactic.

## Quick Start

### Install

```bash
# Via skills CLI (works with 70+ agents: Claude Code, Cursor, Codex, Copilot, Cline, etc.)
npx skills add wlj103/super-spec

# Or clone directly
git clone https://github.com/wlj103/super-spec.git
```

### Trigger

Super-Spec activates automatically when you say any of:
- "Use spec discipline"
- "Execute with Super-Spec"
- "Don't let the AI cut corners"
- "Production-grade delivery"
- "Start a new project with spec"

Or invoke explicitly: `/super-spec`

### First Use

```
1. Have a design document, PRD, or requirements document ready
2. Say: "Use super-spec to execute [document path]"
3. The agent will walk through G0→G1→G2→G3 before writing any code
4. Review the generated Constitution, then approve
5. The agent executes G4→G5→G6 with evidence at every step
```

## How It Works

### The Seven Gates

| Gate | What It Prevents | Pass Condition |
|------|-----------------|----------------|
| **G0: Anchor Review** | Acting without understanding current state | Code facts + confirmed decisions + no-change list, user-confirmed |
| **G1: Decision Points** | Agent filling in defaults on its own | Unconfirmed items prohibited from defaulting; ask user item by item |
| **G2: Constitution** | Understanding drift across sessions | Seven required sections written; five documents implicitly inherit |
| **G3: Five-Document Generation** | Cutting corners, skipping steps, empty verification | Anti-Corner-Cutting Clause + 18-item verification checklist |
| **G4: Progressive Execution** | Declaring completion after one round | ≥3 progressive rounds; all P0 green before proceeding |
| **G5: DoD Final Verification** | Self-deceptive verification | Item-by-item evidence + spot-check 3 ✅ items via different method |
| **G6: Wrap-Up** | Omissions, residual garbage | 12-item wrap-up checklist, verified item by item |

### The Five-Document Interlocking System

```
CONSTITUTION.md  ← Supreme authority; drives everything
      ↓
spec.md          ← What + Why + Scenario (acceptance layer)
      ↔
tasks.md         ← How + Dependencies + Evidence (execution layer)
      ↔
checklist.md     ← Verify + DoD + Anti-Perfunctory (anchor layer)
      ↕
decisions.md     ← Decisions + Pitfalls + Risk Response (knowledge base)
```

Each document has a distinct responsibility. Cross-validation catches drift: if spec says A, tasks cannot say B. Scenario IDs must match across all five documents.

### The Anti-Corner-Cutting Clause

This is the intellectual core of Super-Spec. It catalogs **four categories** of model shortcutting behavior and creates operational definitions to prevent each:

| Category | Examples | How Super-Spec Prevents |
|----------|----------|------------------------|
| **Semi-Structured** | "Exhaustive" → selectively carries over; "Expand" → writes 4 words; "At least N" → shrinks N | Pre-check counting, mandatory templates, operational definitions |
| **Content-Type** | Vague red lines, circular definitions, no baseline numbers, abstract error handling | Per-file red lines, specific definitions, measured baselines, itemized error handling |
| **Structural** | Skipping REMOVED section, no risk list, no File Structure, incomplete Scenario IDs | Mandatory sections, risk response table, File Structure before Tasks, Scenario carry-over |
| **Output Integrity** | Truncation, AIGC metadata, "Yes" without reading files, cross-document inconsistency | Anti-truncation rules, grep for AIGC, verification against actual files, cross-document consistency checks |

## Architecture

```
super-spec/
├── SKILL.md                         # Core skill: 7 gates, 5 documents, anti-corner-cutting
├── README.md                        # This file
├── LICENSE                          # MIT
├── CONTRIBUTING.md                  # Contribution guide
├── CHANGELOG.md                     # Version history
└── references/                      # (optional) Detailed reference docs
    ├── gate-details.md              # Per-gate implementation details
    └── examples.md                  # Real-world execution examples
```

## Design Principles

1. **Constrain behavior, not capability** — Don't instruct on what the model already excels at. Lock down what it shortcuts.
2. **Structural locks, not prompt gates** — Grep-able checklists, cross-document Scenario IDs, non-repudiable evidence.
3. **Divide-and-conquer interlocking** — Five documents cross-validate each other. Drift is detectable.
4. **Constitution-driven, not memory-driven** — Consistency comes from a written document, not model memory.
5. **Probe-driven, not hard-coded** — Ports, paths, dependencies discovered at runtime. Zero environment coupling.
6. **Evidence-based verification, not trust-based** — "Looks fine" does not count. Spot-check with different methods.

## Who This Is For

- **Solo developers** using AI coding agents who need team-level quality assurance without a team
- **AI engineers** who want their agents to follow disciplined engineering practices
- **Project leads** who need verifiable, evidence-backed deliverables from AI agents
- **Anyone who's been burned** by an AI agent confidently delivering broken code

## Compared to Similar Tools

| Tool | Approach | Strengths | When Super-Spec Wins |
|------|----------|-----------|---------------------|
| [spec-driven-development](https://github.com/addyosmani/agent-skills) | 4-phase spec→plan→tasks→implement | Concise, practical, widely adopted | When you need enforcement, not just guidance |
| [sdlc-ai-workflow](https://github.com/saitarrun/sdlc-ai-workflow) | 26 agents across 6 SDLC phases | Comprehensive, industrial-grade | When you want lightweight, not heavy orchestration |
| Anthropic's [skill-creator](https://github.com/anthropics/skills) | Meta-skill for creating skills | Eval-driven, iterative | When you need to prevent corner-cutting in execution |
| **Super-Spec** | **7-gate enforcement + anti-corner-cutting** | **Structural prevention of model shortcutting** | **When "looks fine" is not good enough** |

## Why "Super-Spec"?

The name comes from the core insight: traditional specs are **documents that agents read** (and then ignore). Super-Spec is a **discipline system that agents cannot bypass**. It's "super" not because it's bigger, but because it operates at a higher level — it doesn't tell the agent what to build, it prevents the agent from building it wrong.

## Real-World Impact

Super-Spec was battle-tested in the **V14 Brain Memory Architecture Upgrade** — a production AI infrastructure project with 46 files, 78KB of source code, and 533 test cases:

- **5 documents, 996 lines** generated through the seven-gate pipeline (Constitution + spec + tasks + checklist + decisions)
- **Gate Three 16-item self-check**: all green on first pass, zero false "Yes" answers
- **Cross-document consistency**: Scenario IDs matched across all 5 documents; drift caught before execution
- **Zero unconfirmed defaults**: Gate One surfaced 8 decision points the agent would have silently defaulted
- **Evidence trail**: Every task completion backed by script name + pass count, not claims

In testing across multiple projects, Super-Spec has been shown to:
- **Eliminate** the "tests passed" with zero evidence pattern
- **Prevent** scope drift through Constitution anchoring every round
- **Catch** cross-document inconsistencies before execution begins
- **Enforce** progressive iteration (≥3 rounds) instead of one-and-done
- **Surface** unconfirmed decisions that would otherwise be silently defaulted

## Roadmap

Super-Spec solves the **engineering discipline** problem — preventing AI agents from cutting corners. But there's a second half to the equation:

| Problem | Skill | Status |
|---------|-------|--------|
| AI skips steps, claims success without evidence | **super-spec** — Engineering discipline | ✅ Released |
| AI expresses vaguely, lacks structure, leaves ambiguity | **super-prompt** — Prompt discipline | 🔜 Planned |

Super-Spec ensures the agent **does the right things**. Super-Prompt will ensure the agent **says them the right way** — precise, structured, ambiguity-free. Two sides of the same coin: one enforces how agents execute, the other enforces how agents express.

*Interested in super-prompt? Star this repo and watch for updates.*

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Super-Spec follows [Agent Skills](https://agentskills.io) open standard. PRs welcome for:
- Additional anti-corner-cutting patterns discovered in practice
- New Scenario coverage dimensions
- Platform-specific adaptations
- Documentation improvements

## License

MIT © 2026

---

*Built with the belief that AI agents should earn our trust through evidence, not confidence.*