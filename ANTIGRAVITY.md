# Anti-Gravity 工作規則 (ANTIGRAVITY.md)

> 專案名稱：2026ppt-by-notebooklm
> 用途：從 NotebookLM 匯出的教材/筆記自動生成 HTML 互動簡報及串接 NotebookLM MCP 處理簡報
> 工作資料夾：`d:\antigravity\2026ppt-by-notebooklm`
> 專案筆記 / Obsidian 駕駛艙：`d:\antigravity\2026antigravity\SecondBrain\SecondBrain\Agent_Logs\`

---

## 📌 固定規則與專案邊界

1. **核心原則**：本專案為將 NotebookLM 筆記自動轉換為 HTML 互動簡報（Reveal.js）的自動化工具與展示平台。
2. **進度與日誌記錄**：開發進度、Bug 踩坑、每日紀錄應保存在中央 Obsidian 儲存庫 `d:\antigravity\2026antigravity\SecondBrain\SecondBrain\Agent_Logs\` 下（檔名格式：`2026ppt-by-notebooklm_YYYY-MM-DD_[任務簡述].md`），**不得**直接 commit 至公開庫。
3. **生圖儲存**：生成圖片一律存存放於專案的 `assets/` 目錄中，並加強去背與置中對齊。

---

## 🔒 安全原則 (Do's & Don'ts)

### ✅ Do's (應做事項)
* **NotebookLM 授權**：登入一律通過瀏覽器安全 OAuth（`nlm login`）。
* **憑證隔離**：Firebase 前端 config 可以公開，但 Admin SDK 憑證與任何私鑰均應嚴格置於本地排除範圍。
* **收工檢查**：收工時務必使用 `git status` 與 `git diff` 檢查變更，並撰寫結構化的 commit message，獲得確認後方可提交。
* **精準提交**：僅 Stage 本次任務直接相關的檔案，嚴格過濾敏感變更。

### ❌ Don'ts (嚴禁事項)
* **嚴禁**無差別使用 `git add .`。
* **嚴禁**將 API Keys、GitHub Token、Firebase Admin 憑證等任何明文金鑰寫入 Markdown 或 Git 庫。
* **嚴禁**將 `notebooks.json`、NotebookLM 筆記本 ID 清單、研究報告或生成圖片 commit 到公開/舊 repository 中。
* **嚴禁**在 AntiGravity 中安裝或註冊 `@bitbonsai/mcpvault` 與 Obsidian MCP，保持筆記工作流的免 MCP 安全管理模式。
