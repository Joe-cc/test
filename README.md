# Cursor 設定完整說明

Cursor 有兩套設定介面：

| 介面 | 開啟方式 | 用途 |
|------|----------|------|
| Cursor Settings（AI 專用） | Cmd + Shift + J（Mac）或右上角齒輪 | 模型、Agent、Tab、索引、規則、MCP 等 |
| VS Code Settings（編輯器） | Cmd + , | 字型、主題、格式化、終端機等一般編輯器設定 |

以下以 Cursor Settings 側邊欄各分頁為主，逐項說明。

---

## 1. General（一般）
- **Account（帳戶）**：登入狀態、訂閱方案（Hobby / Pro / Pro Plus / Ultra / Teams）、用量查看、匯入 VS Code 設定。  
- **Privacy Mode（隱私模式）**：程式碼不會被模型供應商用於訓練，支援零資料保留（ZDR）。  
- **其他常見項目**：語言 / 地區、通知、遙測（Telemetry）。

---

## 2. Models（模型）
- **模型選擇**：Auto、Premium、Composer、自研模型、Claude、GPT、Gemini、Grok 等。  
- **API Keys（BYOK）**：可填入 OpenAI、Anthropic、Google 等 API Key。  
- **Max Mode**：上下文擴展到模型上限，適合大型重構。  
- **模型顯示**：可隱藏不常用模型。

---

## 3. Tab（自動完成）
- **基本行為**：啟用/停用 Tab、部分接受、註解/字串觸發。  
- **進階功能**：跨檔案建議、Peek 視圖支援。  
- **狀態列控制**：右下角 Tab 指示器可 Snooze 或停用。

---

## 4. Agent（聊天助手）
- **Run Mode（執行模式）**：Auto-review、Allowlist、Run Everything。  
- **網路存取**：sandbox.json Only / Defaults / Allow All。  
- **Protection（保護設定）**：阻止刪檔、阻止改 dotfile、阻止外部檔案修改。  
- **其他設定**：Agent Stickiness、Auto-scroll、Attribution、Default context。  
- **沙箱（Sandbox）**：受限環境執行指令，設定檔位於 `.cursor/sandbox.json`。

---

## 5. Indexing & Docs（索引與文件）
- **Codebase Indexing**：自動索引、忽略檔案、Git Graph Relationships。  
- **Docs（自訂文件）**：新增外部文件來源，在 Chat 用 `@docs` 引用。

---

## 6. Rules, Commands（規則與命令）
- **User Rules / Project Rules / Team Rules**：不同層級的規則設定。  
- **Commands（自訂命令）**：在 Agent 輸入框用 `/命令名` 觸發。  
- **AGENTS.md / CLAUDE.md**：專案根目錄的指令文件。

---

## 7. Tools & MCP（工具與 MCP）
- **MCP 管理**：顯示伺服器、工具數量、錯誤訊息。  
- **新增 MCP Server**：支援 stdio、SSE 傳輸方式。  
- **工具開關**：可在 Agent 面板啟用/停用 MCP 工具。

---

## 8. Hooks（鉤子）
- **設定位置**：專案 `.cursor/hooks.json` 或全域 `~/.cursor/hooks.json`。  
- **常見 Hook 事件**：sessionStart、beforeSubmitPrompt、preToolUse、afterFileEdit 等。  
- **除錯**：Settings 的 Hooks 分頁可查看紀錄。

---

## 9. Beta（測試版）
- **Update Channel**：Stable / Early Access / Nightly。  
- **實驗功能**：Cursor Browser、Plan Mode、Agent Skills。

---

## 10. Features / Editor / Terminal
- **Editor**：Chat/Edit Tooltip、Auto Parse Links、Themed Diffs。  
- **Terminal**：Show Terminal Hover Hint、Use Preview Box。

---

## 11. VS Code Settings（Cmd + ,）
- **Editor**：字體大小、Tab 寬度、格式化、自動換行。  
- **Workbench**：主題、圖示、顏色模式。  
- **Files**：自動儲存、檔案隱藏。  
- **Terminal**：字體大小。  
- **Git**：自動 fetch。

---

## 設定檔位置速查
- 使用者設定：`~/Library/Application Support/Cursor/User/settings.json`  
- MCP：`~/.cursor/mcp.json`  
- 權限：`~/.cursor/permissions.json`  
- 沙箱：`~/.cursor/sandbox.json`  
- Hooks：`~/.cursor/hooks.json`  
- CLI 設定：`~/.cursor/cli-config.json`

---

## 建議的初始配置
- General → Privacy Mode：處理敏感程式碼時開啟。  
- Models：日常用 Auto；複雜重構再選 Premium 或特定模型。  
- Agent → Run Mode：預設 Auto-review；高風險專案用 Allowlist。  
- Tab：註解寫作時關閉 Trigger in comments。  
- Indexing：大型 monorepo 用 `.cursorignore` / `.cursorindexingignore` 排除無關目錄。  
- Rules：加入語言偏好（如繁體中文）與專案慣例。
