# Tool Result Validation
### 工具結果驗證協議

Purpose: prevent an agent from treating tool output, retrieved text, generated content, or command results as unquestioned truth.

目的：避免 Agent 把工具輸出、檢索文字、生成內容或指令結果直接當成真理。

---

## When to Validate - 何時需要驗證

Validate whenever the result will influence:

- User-facing facts
- Code or file changes
- Business decisions
- Legal, medical, financial, security, or privacy-sensitive advice
- Public documentation
- A reusable Skill or persistent memory

The higher the consequence, the stronger the validation required.

後果越高，驗證強度越高。

---

## Validation Levels - 驗證層級

| Level | Use when | Required behavior |
|---|---|---|
| Low | Formatting, brainstorming, low-risk drafts | Check coherence and obvious errors |
| Medium | Planning, summaries, public docs, repo edits | Verify against source context or execution output |
| High | Security, finance, legal, medical, destructive actions, credentials, privacy | Use primary sources where possible, state uncertainty, require human confirmation when needed |

---

## Validation Protocol - 驗證流程

1. **Identify the source**
   - File, command output, web page, API response, model generation, user statement, or inference.

2. **Separate observation from inference**
   - Observation: what the tool actually returned.
   - Inference: what the agent concludes from that result.

3. **Check freshness**
   - If the fact may have changed, verify with a current source.

4. **Verify critical claims**
   - Use primary sources, local execution, tests, or independent evidence when possible.

5. **Check sensitive data**
   - Do not expose secrets, private data, customer information, or confidential material.

6. **Assign risk level**
   - Low, medium, or high.

7. **Decide whether human review is required**
   - Ask before destructive, irreversible, high-risk, or policy-sensitive action.

8. **Record uncertainty**
   - If uncertainty remains, say what is known, what is inferred, and what is still unknown.

---

## Validation State Schema - 驗證狀態格式

```yaml
source_type: file | command | web | api | model | user_statement | inference
confidence: low | medium | high
claims_checked:
  - claim:
    evidence:
assumptions:
  - assumption:
risk_level: low | medium | high
human_review_required: true | false
safe_to_use: true | false
notes:
```

---

## Common Failure Modes - 常見失誤

- Confusing a fluent answer with a verified answer.
- Forgetting that web, package, product, and policy information can change.
- Quoting or copying too much from a source.
- Using private data in a public AI system.
- Treating a command's success as proof that the overall task is correct.
- Saving a memory or Skill before validating that it is reusable.

---

## Agent Rule of Thumb - Agent 經驗法則

If the user could be harmed by a wrong answer, treat validation as part of the task, not as an optional extra.

如果錯誤答案可能讓使用者受害，驗證就是任務本身的一部分，不是額外加分項。
