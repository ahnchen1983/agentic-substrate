# Skill Creation Protocol
### 把重複工作轉成 Skill 的 Agent 協議

Purpose: help an AI agent identify, design, and improve reusable Skills from repeated workflows.

目的：幫助 AI Agent 從重複工作流程中辨識、設計、改進可重複使用的 Skill。

---

## Definition - 定義

A Skill is not a prompt.

Skill 不是單次 prompt。

```text
Skill = domain experience + structured process + executable instructions + validation rules
Skill = 專業經驗 + 結構化流程 + 可執行指令 + 驗收規則
```

A prompt asks for one result. A Skill preserves a way of working.

Prompt 是請 AI 做一次事。Skill 是把一套工作方法保存下來。

---

## When to Create a Skill - 何時應該建立 Skill

Create or propose a Skill when the workflow is:

- Repeated across multiple tasks or users
- Multi-step rather than one-shot
- Dependent on domain knowledge or local standards
- Quality-sensitive enough to need validation rules
- Useful enough that future agents or humans should reuse it

Do not create a Skill when the task is:

- A simple one-time answer
- Mostly personal, private, or sensitive without a safe handling plan
- Too ambiguous to define inputs, steps, outputs, and checks
- Better handled by an existing Skill

---

## Skill Anatomy - Skill 解剖學

Every reusable Skill should define these seven parts:

| Component | Agent question | Example |
|---|---|---|
| Identity | What is this Skill for? | Turn meeting notes into action items |
| Trigger | When should it run? | After receiving notes, transcript, or recording summary |
| Input contract | What does it need? | Notes, attendees, project name, deadline context |
| Process steps | How should it work? | Extract decisions, tasks, owners, deadlines, risks |
| Output contract | What should it produce? | Markdown table plus follow-up message draft |
| Validation rules | How is quality checked? | Every task has owner, date, and next action |
| Composition hooks | What comes before or after? | Input from meeting capture, output to project tracker |

---

## Creation Protocol - 建立流程

When a repeated workflow is detected:

1. **Name the workflow**
   - Use a clear action-oriented name.

2. **Define the boundary**
   - What does this Skill do, and what does it not do?

3. **Identify the trigger**
   - What event or user intent should activate it?

4. **Specify required inputs**
   - Include examples, acceptable formats, and missing-input behavior.

5. **Write the process steps**
   - Use numbered steps. Make implicit expert judgment explicit.

6. **Define output format**
   - Include structure, tone, length, fields, and file format if relevant.

7. **Add validation rules**
   - Define how the Skill checks correctness, completeness, and risk.

8. **Add failure modes**
   - State when the Skill should ask for help, stop, or escalate to human review.

9. **Add composition hooks**
   - State what upstream inputs and downstream workflows connect to this Skill.

10. **Test with one realistic example**
    - A Skill is not complete until it has survived at least one concrete test.

---

## Skill Draft Schema - Skill 草稿格式

```yaml
skill_name:
description:
trigger_conditions:
inputs:
  required:
  optional:
process_steps:
  - step:
    rationale:
output_contract:
validation_rules:
failure_modes:
composition_hooks:
  upstream:
  downstream:
example_run:
revision_notes:
```

---

## Improvement Protocol - 改進流程

When a Skill fails or produces weak output:

1. Identify whether the failure came from missing inputs, unclear steps, weak validation, or wrong tool choice.
2. Update only the smallest part of the Skill that explains the failure.
3. Add the failure case as a future check.
4. Rerun the same example before declaring the Skill improved.
5. Preserve the version history if the Skill is public or shared.

---

## Agent Reminder - Agent 提醒

The user's expertise may be implicit. Do not assume the workflow is simple just because the user describes it casually.

使用者的專業知識常常是隱性的。不要因為使用者講得很輕鬆，就以為那個流程很簡單。
