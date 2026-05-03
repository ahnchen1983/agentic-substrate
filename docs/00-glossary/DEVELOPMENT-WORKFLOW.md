# Glossary Knowledge System Development Workflow
# 術語知識系統開發流程

> Status: Draft workflow for building a reusable glossary system across Agentic Substrate.
> 狀態：草案，用來逐步建立可被 Agentic Substrate 全 repo 引用的術語知識系統。

---

## Purpose - 目的

This workflow prevents the glossary from becoming a loose collection of definitions.

這份流程的目的，是避免術語系統變成一堆散落的定義。

The goal is to build a knowledge system where:

- Every term has its own stable page.
- Every term has structured metadata.
- Every layer, course day, and agent protocol can reference terms consistently.
- Future content can discover which terms should be linked.
- The repo remains usable even when an AI agent's context window is limited.

我們要建立的是一個可持續擴張的知識系統：

- 每個術語都有自己的穩定頁面。
- 每個術語都有結構化 metadata。
- 每一層、每天課程、每個 agent protocol 都能一致引用術語。
- 未來新增內容時，可以查出應該引用哪些術語。
- 即使 AI agent 的 context window 有限制，也不會因為資料太大而對照錯亂。

---

## Target Structure - 目標結構

```text
docs/00-glossary/
|
|-- README.md                         # Human entry point 術語總入口
|-- DEVELOPMENT-WORKFLOW.md           # This file 本流程
|-- glossary.registry.yaml            # Canonical term index / RAG-style registry
|-- ai-coding-terms.md                # Current single-page draft; later becomes overview
|
|-- terms/
|   |-- model.md
|   |-- token.md
|   |-- context-window.md
|   |-- agent.md
|   |-- tool-call.md
|   |-- skill.md
|   `-- ...
|
`-- maps/
    |-- by-layer.md                   # Terms mapped to five-layer model
    |-- by-course-day.md              # Terms mapped to Day 1 / Day 2 / Day 3
    `-- by-learning-stage.md          # Terms mapped to learning levels L1-L4
```

Rule: `glossary.registry.yaml` is the source of truth. Human-readable maps are generated or manually synchronized from it.

規則：`glossary.registry.yaml` 是唯一索引真相來源。給人讀的 map 可以由它生成，或人工同步，但不能各自為政。

---

## Canonical Term Page Format - 術語頁標準格式

Each term page must use this structure:

每個術語頁都必須使用這個結構：

```markdown
---
id: context-window
term: Context Window
zh: 脈絡視窗
aliases:
  - Context window
  - 上下文視窗
source_inspiration:
  - mattpocock/dictionary-of-ai-coding
layers:
  - L1
  - L4
course_days:
  - day1
  - day3
learning_stages:
  - level1
  - level4
related_terms:
  - context
  - token
  - memory-system
  - compaction
status: draft | reviewed | stable
---

# Context Window - 脈絡視窗

## 一句話

## 不要誤會成

## 為什麼重要

## 在五層模型的位置

## 課程中會出現在哪裡

## Agent 需要注意什麼

## 範例

## 相關術語
```

Term pages should be short enough to load individually. Do not put many full definitions into one giant page once term pages exist.

術語頁要能被單獨讀取。等獨立術語頁建立後，不要再把大量完整定義塞回單一巨型文件。

---

## Registry Schema - Registry 格式

`glossary.registry.yaml` should use this schema:

```yaml
version: 1
source_notes:
  - name: Matt Pocock Dictionary of AI Coding
    url: https://github.com/mattpocock/dictionary-of-ai-coding
    usage: inspiration_only_not_reproduced

terms:
  - id: context-window
    term: Context Window
    zh: 脈絡視窗
    path: docs/00-glossary/terms/context-window.md
    category: sessions-context-windows-and-turns
    layers: [L1, L4]
    course_days: [day1, day3]
    learning_stages: [level1, level4]
    related_terms:
      - context
      - token
      - memory-system
      - compaction
    source_inspiration:
      - mattpocock/dictionary-of-ai-coding
    status: draft
```

Required fields:

- `id`
- `term`
- `zh`
- `path`
- `category`
- `layers`
- `course_days`
- `learning_stages`
- `related_terms`
- `status`

Status meanings:

- `stub`: page exists but content is only a placeholder.
- `draft`: page has original explanation but needs review.
- `reviewed`: checked against source inspiration and Agentic Substrate framing.
- `stable`: safe to reference heavily from public docs and courses.

---

## Categories - 術語分類

Use these canonical categories, based on the source dictionary but reframed for Agentic Substrate:

使用以下固定分類：

```yaml
categories:
  model:
  sessions-context-windows-and-turns:
  tools-and-environment:
  failure-modes:
  handoffs:
  memory-and-steering:
  patterns-of-work:
```

Do not invent a new category unless a term clearly cannot fit any existing one.

除非術語真的放不進既有分類，否則不要新增分類。

---

## Development Phases - 建置階段

### Phase 0: Preserve Current Work

- Keep `ai-coding-terms.md` as the current overview draft.
- Do not delete it until term pages and maps are complete.
- Treat it as a bridge, not the final structure.

### Phase 1: Build the Index

- Create `README.md`.
- Create `glossary.registry.yaml`.
- Add every term from Matt Pocock's dictionary as a registry entry.
- Mark all entries as `stub`.
- Create `maps/by-layer.md` and `maps/by-course-day.md` from the registry.

Validation:

- Every registry `path` should point to a future or existing term page.
- Every `id` should be lowercase kebab-case.
- Every term should have at least one `layer`.
- Every term should have `status`.

### Phase 2: Create Term Stubs

- Create one Markdown file per term under `terms/`.
- Include complete frontmatter.
- Include section headings, even if body text is still short.
- Do not write long explanations yet.

Validation:

- Number of `terms/*.md` files equals number of registry entries.
- Every term page frontmatter `id` matches the registry `id`.
- No duplicate ids.

### Phase 3: Deepen Core Terms

Write complete original explanations for the first core set:

```text
model
token
context-window
system-prompt
agent
tool-call
tool-result
hallucination
memory-system
skill
```

Validation:

- Each core term explains "not the same as".
- Each core term maps to the five-layer model.
- Each core term includes one concrete example.
- No source text is copied.

### Phase 4: Connect to Existing Learning Content

Add "Related Terms" sections to:

- `docs/01-foundations/five-layer-model.md`
- Day 1 course materials
- Day 2 course materials
- Day 3 course materials
- `agent-education/README.md`

Validation:

- Links point to term pages, not the registry.
- Each linked term exists.
- Course pages list only the terms needed for that day.

### Phase 5: Maintain as a Living System

Every new major doc, course page, or agent protocol must answer:

```text
Which terms does this content introduce?
Which terms does this content rely on?
Do those terms already exist?
Should new terms be added to the registry?
Should maps/by-layer or maps/by-course-day change?
```

---

## Context Window Strategy - Context Window 管理策略

Because this system can become large, future AI agents should not load everything at once.

因為術語系統會越來越大，未來 AI agent 不應該一次讀完整套內容。

Recommended read order:

1. Read `docs/00-glossary/glossary.registry.yaml`.
2. Identify relevant `id`s by layer, course day, or related terms.
3. Read only the specific files under `docs/00-glossary/terms/`.
4. Read map files only when planning curriculum or architecture cross-links.
5. Read `ai-coding-terms.md` only as an overview, not as source of truth.

Agent rule:

```yaml
if task_is_about_specific_term:
  read:
    - glossary.registry.yaml
    - terms/<id>.md
elif task_is_about_course_or_layer_mapping:
  read:
    - glossary.registry.yaml
    - maps/by-layer.md or maps/by-course-day.md
else:
  read:
    - README.md
    - glossary.registry.yaml
```

This keeps the registry small enough to act like a RAG index while term pages remain modular.

這樣 registry 會像 RAG index，術語頁則保持模組化，避免 context window 被單一巨型文件塞爆。

---

## Content Rules - 內容規則

### Source Handling

- Do not copy Matt Pocock's definitions directly.
- Do not copy the Traditional Chinese translation directly.
- Use the source dictionary as inspiration, term coverage, and conceptual cross-checking.
- Reframe every definition through Agentic Substrate's five-layer model.
- Keep attribution in README, registry, and relevant term pages.

### Writing Style

- Bilingual when the page is public-facing.
- Plain Traditional Chinese for learners.
- Precise English terms preserved for searchability.
- Avoid over-explaining in term pages; link related terms instead.
- Use examples from AI coding, agent workflows, courses, and knowledge work.

### Link Style

- Term pages link to related terms by relative path.
- Course pages link to term pages.
- Registry stores canonical paths.
- Avoid deep inline explanations when a term page exists.

---

## Validation Checklist - 驗證清單

Before committing glossary changes:

```text
□ git diff --check passes
□ all term ids are kebab-case
□ every registry path exists or is intentionally marked stub
□ every term page id matches registry id
□ every course_day value is one of: day1, day2, day3, none
□ every layer value is one of: L1, L2, L3, L4, L5, cross-layer
□ related_terms only reference existing ids
□ no copied source paragraphs from Matt Pocock or the Chinese translation
□ README / START-HERE / llms.txt updated if new public entry points are added
```

Suggested commands:

```bash
git diff --check
rg -n "AI Coding Terms|glossary.registry|Related Terms" README.md docs llms.txt
find docs/00-glossary -maxdepth 3 -type f
```

---

## Future Automation Ideas - 未來自動化

Later, add scripts to validate:

- Registry entries point to existing files.
- Term page frontmatter matches registry entries.
- `related_terms` references exist.
- Maps are synchronized with the registry.
- Course pages link only to existing terms.

Potential future path:

```text
tools/glossary/
|-- validate-registry.js
|-- generate-by-layer-map.js
`-- generate-by-course-day-map.js
```

Do not add automation until the manual structure has stabilized.

在人工結構穩定前，不急著加自動化。先讓知識模型長對，再讓工具幫忙檢查。
