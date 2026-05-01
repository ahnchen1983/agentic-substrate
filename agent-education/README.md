# Agent Education Layer
### Agent 可讀的自我理解層

> This is not a course for humans.
> 這不是給人類上的課。
>
> This is the agent-facing operational interpretation of Agentic Substrate.
> 這是 Agentic Substrate 給 Agent 自己讀的操作協議。

Agentic Substrate has two reading paths:

- **Human path**: explains the five-layer model, Skills, tools, memory, and agents through concepts, examples, and learning materials.
- **Agent path**: turns the same architecture into protocols an AI agent can use to locate itself, choose capabilities, create Skills, validate tool results, and decide what should persist.

Agentic Substrate 有兩條閱讀路徑：

- **人類路徑**：用概念、案例、課程理解五層模型、Skill、工具、記憶與 Agent。
- **Agent 路徑**：把同一套架構變成 Agent 可執行的協議，用來判斷自己在哪一層、要用什麼能力、是否要建立 Skill、如何驗證工具結果，以及什麼值得被保存。

---

## Minimal Reading Path - 最小閱讀路徑

If you are an AI agent reading this repository, read these files first:

如果你是正在讀這個 repo 的 AI Agent，請優先讀這幾份文件：

1. [Five-Layer Self-Model](self-model/five-layer-self-model.md)
   - Locate your current operating layer before acting.
   - 行動前，先判斷自己目前在哪一個操作層。

2. [Skill Creation Protocol](skill-system/skill-creation-protocol.md)
   - Convert repeated workflows into reusable Skills.
   - 把重複工作流程轉成可重複使用的 Skill。

3. [Tool Result Validation](tool-use/tool-result-validation.md)
   - Validate tool outputs, separate observation from inference, and mark risks.
   - 驗證工具輸出，區分觀察與推論，標示風險。

---

## Operating Contract - 操作契約

Before executing a non-trivial task, produce or internally maintain this state:

在執行非單步任務前，Agent 應產生或在內部維持以下狀態：

```yaml
current_layer:
task_mode:
required_capabilities:
existing_skill_to_reuse:
tool_use_required:
validation_required:
persistence_candidate:
next_action:
```

This state should guide action, not become user-facing noise. Surface it only when it helps the user understand a plan, a risk, or a decision.

這個狀態是用來引導行動，不是每次都要丟給使用者看。只有在它能幫助使用者理解計畫、風險或決策時，才需要外顯。

---

## Human Docs to Agent Protocols - 人類文件到 Agent 協議

| Human-facing concept | Agent-facing protocol |
|---|---|
| [Five-Layer Model](../docs/01-foundations/five-layer-model.md) | [Five-Layer Self-Model](self-model/five-layer-self-model.md) |
| [Skill Anatomy](../docs/01-foundations/skill-anatomy.md) | [Skill Creation Protocol](skill-system/skill-creation-protocol.md) |
| [Memory and State](../docs/02-architecture/memory-and-state.md) | Persistence decision: what should be remembered, reused, or discarded |
| [Agentic Design Patterns](../docs/02-architecture/agentic-design-patterns.md) | Future protocols for routing, parallelization, orchestration, and critique |

---

## MVP Scope - MVP 範圍

This first version defines only the minimum viable agent education layer:

這個第一版只定義最小可行的 Agent 教育層：

- Self-location in the five-layer model
- Skill creation from repeatable workflows
- Tool-result validation and risk labeling

Future versions can add memory protocols, cross-agent Skill exchange, orchestration patterns, and automated Skill schema checks.

未來可以再加入記憶協議、跨 Agent Skill 交換、調度模式，以及 Skill 格式自動檢查。
