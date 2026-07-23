# Super-Spec: Spec-Driven Engineering Discipline for AI Coding Agents

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Standard: Agent Skills](https://img.shields.io/badge/Standard-Agent%20Skills-6e3ef7.svg)](https://agentskills.io)
[![Platform: Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-orange.svg)](https://claude.ai)

[![Star History Chart](https://api.star-history.com/svg?repos=wlj103/super-spec&type=Date)](https://star-history.com/#wlj103/super-spec&Date)
[![Platform: Cursor](https://img.shields.io/badge/Cursor-Compatible-000.svg)](https://cursor.com)
[![Platform: Codex](https://img.shields.io/badge/OpenAI%20Codex-Compatible-74aa9c.svg)](https://openai.com)


> 🛡️ **先写规范，再写代码。AI 也不例外。** — 防AI偷懒、防AI作弊、防AI跳步。每一步都锁死，缺证据就重来。个人开发者也能拥有团队级质量。
**Stop vibe coding. Start spec driving.** Super-Spec is the engineering discipline layer for AI coding agents — specification-first, verification-always. Anti-corner-cutting, evidence-based verification, structural locks. Production-grade quality gates for AI-generated code. Built for solo developers.

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
## The Problem: AI Keeps Skipping Steps

AI coding agents are technically brilliant but behaviorally undisciplined. They **skip requirements**, **fill in defaults without asking**, **claim "tests passed" with zero evidence**, and deliver results that "look fine" but break in production.

This is the **70% Problem** — AI gets you 70% there fast, but the last 30% is where production readiness lives. And prompt engineering doesn't fix it. Models learn to circumvent prompts — "enforce verification rigorously" becomes four words in the output: "Verification enforced rigorously."

**Super-Spec is not a prompt. It's a structural enforcement system.** It's the engineering discipline that AI agents are missing — specification-first, verification-always, evidence-based.

## Key Features — What Makes This Unique / 核心功能 — 别人没有的

Super-Spec is the only agent skill that **systematically catalogs how AI models cut corners** and creates **operational definitions** to prevent each tactic.

Super-Spec 是唯一一个系统性地**分类模型如何偷懒**、并为每种偷懒手段创建**操作定义**来阻止的 Agent Skill。

| Feature 功能 | The Problem It Solves 解决什么问题 | What People Actually Search 用户会搜什么 |
|---------|---------------|------------------------|
| **Anti-Corner-Cutting 反偷懒条款** | AI keeps skipping steps, fills in defaults, claims done without evidence | "AI keeps skipping steps" / "AI总跳步骤怎么办" / "AI偷懒不按流程" / "stop AI cutting corners" |
| **Cross-Document Validation 文档交叉验证** | AI code drifts from requirements; spec says one thing, code does another | "AI code doesn't match requirements" / "AI代码和需求不一致" / "AI不按需求开发" / "AI ignores spec" |
| **Constitution-Driven 规则驱动** | AI forgets context between rounds; each session starts from scratch | "AI forgets context" / "AI忘记上下文" / "AI不记得之前的约定" / "make AI follow rules consistently" |
| **Evidence-Based Verification 证据验证** | AI says "tests passed" but never actually ran them; zero proof of work | "AI says tests passed but didn't" / "AI谎称测试通过" / "AI测试没跑就说通过" / "verify AI actually ran tests" |
| **Solo Developer Workflow 单人团队级质量** | No reviewer, no QA, no PM — just you and AI. How to get production-grade quality alone? | "solo developer AI coding" / "个人开发者用AI写代码" / "没有代码审查的AI开发" / "一个人用AI做项目" |
| **Structural Locks 结构锁** | AI bypasses prompts; writes "enforcement applied" but skips the actual work | "AI bypasses prompts" / "AI绕过提示词" / "提示词管不住AI" / "AI ignores instructions" |
| **Spot-Check Re-Verification 抽查复验** | AI output looks fine but breaks in production; surface-level validation misses real bugs | "AI looks fine but breaks" / "AI表面没问题实际有bug" / "AI自欺欺人" / "verify AI output is real" |
| **Pre-Flight + Rollback 预检+回滚** | AI deployment broke everything, no way to recover; destructive operations with no safety net | "AI deployment broke everything" / "AI部署搞崩了" / "AI操作失误无法恢复" / "safe AI deployment rollback" |
| **Progressive ≥3 Rounds 渐进式迭代** | AI stops after first attempt, declares "done" when quality is still poor | "AI stops after first attempt" / "AI只做一轮就说完成" / "AI不迭代优化" / "AI doesn't iterate" |
| **Seven-Gate Pipeline 七步质量流水线** | No structured workflow for AI coding; ad-hoc prompts lead to ad-hoc quality | "production-grade AI code" / "AI代码如何达到生产级" / "AI工程化开发流程" / "AI coding workflow quality" |

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

### Why Not Just Prompt Engineering?

| Approach | What Happens |
|----------|-------------|
| "Write a good prompt" | AI writes "Good prompt followed" — then skips steps anyway |
| "Add verification rules" | AI writes "Verification rules applied" — no evidence |
| "Use a longer system prompt" | Models ignore long prompts; context is diluted |
| **Super-Spec (structural)** | Grep-able checklists, Scenario IDs, cross-document locks — cannot be bypassed |

Prompts are requests. Super-Spec is architecture. **You can't talk an AI out of cutting corners — you have to build a structure it can't circumvent.**

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

- **Solo developers** using AI coding agents — get team-level quality assurance without a team, reviewer, or QA
- **Vibe coders who've been burned** — you shipped fast, then spent weeks fixing AI-generated bugs. Never again.
- **AI engineers** who want their agents to follow disciplined engineering practices with evidence
- **Project leads** who need verifiable, evidence-backed deliverables from AI agents
- **Anyone tired of AI cutting corners** — "tests passed" without proof, requirements skipped, defaults filled in silently

## Compared to Similar Tools

### Super-Spec vs Vibe Coding

| | Vibe Coding 🎤 | Super-Spec 🛡️ |
|---|------------|------------|
| **Philosophy** | "Just describe it, AI figures it out" | "Spec first, verify always, evidence required" |
| **Speed (first hour)** | 🚀 Fast | 🐢 Slower start |
| **Speed (day 3+)** | 🐌 Slows down (refactoring, bug fixing) | 🚀 Steady, predictable |
| **Risk of production incidents** | High (15-20%事故率) | Low (evidence-anchored) |
| **Understanding debt** | Accumulates silently | Zero — Constitution anchors every round |
| **Best for** | Prototypes, MVPs, exploration | Production, complex systems, long-term maintenance |

### Super-Spec vs Other Spec Tools

| Tool | Approach | Strengths | When Super-Spec Wins |
|------|----------|-----------|---------------------|
| [spec-driven-development](https://github.com/addyosmani/agent-skills) | 4-phase spec→plan→tasks→implement | Concise, practical, widely adopted | When you need enforcement, not just guidance |
| [github/spec-kit](https://github.com/github/spec-kit) | CLI-driven SDD with constitution | 105K stars, GitHub official | When you need structural anti-corner-cutting, not just phase gates |
| [guard-skills](https://github.com/amElnagdy/guard-skills) | Post-hoc quality gates | Second-pass review, catches AI code smells | When you want discipline built-in, not patched-on after |
| Anthropic's [skill-creator](https://github.com/anthropics/skills) | Meta-skill for creating skills | Eval-driven, iterative | When you need to prevent corner-cutting in execution |
| **Super-Spec** | **Specification-first + verification-always** | **Structural prevention of model shortcutting** | **When "looks fine" is not good enough** |

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