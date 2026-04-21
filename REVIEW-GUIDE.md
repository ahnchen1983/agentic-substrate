# Agentic Substrate — 驗證校對指引

> **給 AI 助手的指令：** 請依照本指引，逐一檢查以下所有檔案。每個檢查項目完成後回報結果（✅ 通過 / ⚠️ 需修正 + 具體說明）。最後產出一份總結報告。

---

## 一、整體結構驗證

請確認以下 35 個檔案都存在且非空：

### 根目錄 (7)
- `README.md`
- `QUICK-START.md`
- `ROADMAP.md`
- `CHANGELOG.md`
- `CONTRIBUTING.md`
- `LICENSE`
- `install.sh`

### 設定檔 (3)
- `.claude-plugin/plugin.json`
- `.cursor-plugin/plugin.json`
- `.gitignore`

### 互動視覺化 (1)
- `index.html`

### docs/01-foundations/ (4)
- `agentic-substrate.md` — 核心架構文件
- `skill-anatomy.md` — 技能模組解剖學
- `five-layer-model.md` — 五層架構模型
- `markdown-as-medium.md` — Markdown 作為原生媒介

### docs/02-architecture/ (4)
- `agentic-design-patterns.md` — 代理型設計模式
- `skill-composition.md` — Skill 組合模式
- `memory-and-state.md` — 記憶與狀態管理
- `landscape.md` — 生態系比較分析

### docs/03-claude-case-study/ (1)
- `claude-architecture.md` — Claude 作為活案例

### docs/04-curriculum/ (6)
- `learning-path.md` — 學習路徑總覽
- `you-already-know.md` — 非技術者入口
- `level-1-conversation.md` — Level 1 對話技巧
- `level-2-tools.md` — Level 2 工具使用
- `level-3-skills.md` — Level 3 Skill 建構
- `level-4-agents.md` — Level 4 Agent 調度

### skills/ — 3 個核心 Skill
- `skills/skill-self-discovery/SKILL.md`
- `skills/conversation-to-skill/SKILL.md`
- `skills/skill-builder/SKILL.md`

### skills/examples/ — 6 個範例 Skill
- `skills/examples/meeting-notes-to-actions/SKILL.md`
- `skills/examples/document-reviewer/SKILL.md`
- `skills/examples/research-and-summarize/SKILL.md`
- `skills/examples/project-status-tracker/SKILL.md`
- `skills/examples/accounting-reconciler/SKILL.md`
- `skills/examples/content-pipeline/SKILL.md`

---

## 二、內容品質檢查（逐檔進行）

對每個 `.md` 檔案，請檢查：

### 2.1 語言與文法
- [ ] 英文部分：拼字正確、文法通順、無 Chinglish
- [ ] 中文部分：用語自然、無機翻感、繁體中文（非簡體）
- [ ] 雙語一致性：中英文段落表達的意思一致（不需要逐字翻譯，但概念要對齊）
- [ ] 標點符號：中文用全形標點（，。、；：「」），英文用半形
- [ ] 無亂碼或特殊字元異常

### 2.2 Markdown 格式
- [ ] 標題層級合理（# → ## → ### 不跳級）
- [ ] 程式碼區塊有正確的語言標記（```bash, ```markdown 等）
- [ ] 表格對齊、欄位完整、無破損
- [ ] 連結語法正確 `[text](url)`
- [ ] 清單格式一致（全用 `-` 或全用 `*`，不混用）
- [ ] YAML frontmatter（僅 SKILL.md 需要）格式正確

### 2.3 內容準確性
- [ ] 「五層模型」名稱一致使用：Interface Layer → LLM Layer → Tool Layer → Skill Layer → Agent Layer
- [ ] 「七個組件」名稱一致：Identity, Trigger, Process Logic, I/O Contract, Validation Rules, Knowledge, Composition Hooks
- [ ] 「五種 Skill 類型」名稱一致：Data, Process, Transform, Integration, Orchestration
- [ ] 「四個學習層級」名稱一致：Level 1 Conversation → Level 2 Tool Use → Level 3 Skill Building → Level 4 Agent Orchestration
- [ ] 版本號統一為 `0.2.0`
- [ ] 作者資訊統一為 `Ahn Chen` 和 `Claude (Opus 4.6)`

---

## 三、內部連結驗證

請檢查所有 `.md` 檔案中的相對連結是否指向存在的檔案：

### README.md 中的連結
- `QUICK-START.md` → 存在？
- `docs/01-foundations/agentic-substrate.md` → 存在？
- `docs/01-foundations/skill-anatomy.md` → 存在？
- `docs/01-foundations/markdown-as-medium.md` → 存在？
- `docs/04-curriculum/you-already-know.md` → 存在？
- `docs/02-architecture/landscape.md` → 存在？
- `ROADMAP.md` → 存在？
- `index.html` → 存在？

### QUICK-START.md 中的連結
- `docs/01-foundations/agentic-substrate.md` → 存在？
- `docs/01-foundations/skill-anatomy.md` → 存在？
- `docs/04-curriculum/learning-path.md` → 存在？
- `docs/03-claude-case-study/claude-architecture.md` → 存在？
- `docs/02-architecture/landscape.md` → 存在？
- `index.html` → 存在？

### 各文件之間的交叉引用
- 請掃描所有 `.md` 中 `](` 開頭的相對路徑連結
- 確認每個連結目標檔案存在
- 注意路徑層級是否正確（docs 內的文件引用彼此時路徑前綴）

---

## 四、SKILL.md 專項驗證

對全部 9 個 SKILL.md，請檢查：

### 4.1 YAML Frontmatter
```yaml
---
name: skill-name          # 必填，需與資料夾名稱一致
description: |            # 必填，需包含觸發詞
  ...
metadata:                 # 選填但建議有
  version: "1.0"
  type: Process|Transform|Data|Integration|Orchestration
  domain: ...
---
```
- [ ] `name` 與資料夾名稱一致
- [ ] `description` 有觸發詞（中英皆有更好）
- [ ] `type` 是五種之一

### 4.2 七個組件完整性
每個 SKILL.md 應涵蓋這七個組件（不一定要用同樣的標題名，但概念要有）：
1. **Identity** — 這個 Skill 是什麼、做什麼
2. **Trigger** — 什麼時候該啟動
3. **Process Logic** — 執行步驟
4. **I/O Contract** — 輸入什麼、輸出什麼
5. **Validation Rules** — 品質檢查標準
6. **Knowledge** — 領域知識、規則、範例
7. **Composition Hooks** — 如何與其他 Skill 串接

### 4.3 可讀性
- [ ] 非工程師能理解主要流程
- [ ] 有具體範例或示範
- [ ] 中英文都有（至少關鍵段落雙語）

---

## 五、Plugin 設定驗證

### .claude-plugin/plugin.json
```json
{
  "name": "agentic-substrate",
  "version": "0.2.0",
  "description": "...",
  "author": { "name": "Ahn Chen & Claude (Opus 4.6)" },
  "skills": [{ "path": "skills" }],
  "keywords": [...]
}
```
- [ ] JSON 格式合法
- [ ] version 與 CHANGELOG 一致
- [ ] skills path 指向正確目錄

### .cursor-plugin/plugin.json
- [ ] 與 .claude-plugin 版本一致
- [ ] 有 `compatibility.cursor` 欄位

---

## 六、特殊檔案驗證

### install.sh
- [ ] shebang 正確 (`#!/usr/bin/env bash`)
- [ ] `set -euo pipefail`
- [ ] GitHub URL 為 `https://github.com/ahnchen1983/agentic-substrate`（非 placeholder）
- [ ] 三個安裝選項邏輯正確
- [ ] 有驗證步驟（計算安裝的 SKILL.md 數量）

### index.html
- [ ] 可在瀏覽器獨立開啟（無外部依賴或僅用 CDN）
- [ ] 包含五層模型互動視覺化
- [ ] 包含學習路徑時間線
- [ ] Footer 連結為 `https://github.com/ahnchen1983/agentic-substrate`
- [ ] 雙語顯示

### LICENSE
- [ ] 包含 CC BY-SA 4.0 和 MIT 雙授權

---

## 七、GitHub 呈現預覽

想像這個 repo 在 GitHub 上被人第一次看到：

- [ ] README.md 第一眼是否清楚傳達「這是什麼、為什麼重要、如何開始」
- [ ] 目錄結構是否完整反映實際檔案
- [ ] 「Start Here」區塊的連結是否引導新人到正確的文件
- [ ] 是否有任何 TODO、FIXME、PLACEHOLDER、YOUR_REPO 等殘留標記

---

## 八、輸出格式

完成驗證後，請產出以下格式的報告：

```markdown
# 驗證校對報告

## 總覽
- 檔案數量：X / 35
- 通過項目：X
- 需修正項目：X
- 建議改善：X

## 需修正（必須修）
1. [檔案名] 問題描述 → 建議修正方式
2. ...

## 建議改善（可選）
1. [檔案名] 建議內容
2. ...

## 逐檔檢查結果
| 檔案 | 語言 | 格式 | 連結 | 內容 | 總評 |
|------|------|------|------|------|------|
| README.md | ✅ | ✅ | ✅ | ✅ | PASS |
| ... | ... | ... | ... | ... | ... |
```

---

*本驗證指引由 Agentic Substrate 專案產出，版本 0.2.0*
