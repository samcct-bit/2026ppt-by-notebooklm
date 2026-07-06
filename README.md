# 🎨 2026ppt-by-notebooklm

> 從 NotebookLM 匯出的教材/筆記自動生成 HTML 互動簡報及串接 NotebookLM MCP 處理簡報。

## 🚀 專案介紹
本專案專為自動化教學簡報設計，能將 NotebookLM 的輸出內容快速轉化為高品質、可即時互動的 Reveal.js HTML 簡報，並支援底圖 AI 生成、Firebase 互動（如即時文字雲、單選投票等），以及一鍵部署至 GitHub Pages。

## 🛠 功能特點
- 📂 **NotebookLM 整合**：透過 `nlm` CLI 工具與 NotebookLM MCP 處理並同步教材。
- 🖼 **AI 暗霓虹底圖**：整合 Image 2 生成高質感暗霓虹風格底圖，兼顧視覺張力。
- 💬 **Firebase 即時互動**：簡報內建互動元件（如 Firebase Firestore 串接的即時文字雲與即時投票）。
- 🔀 **Reveal.js 動態展示**：支援響應式排版、圖表、SVG 向量圖與對比滑桿效果。
- 🚀 **GitHub Pages 部署**：自動推送至 GitHub 並透過 GitHub Pages 進行公開分享。

## 🔧 快速開始
1. **驗證環境與登入**
   ```bash
   nlm login
   ```
2. **安裝必要套件**
   本專案開發建議使用 Python 虛擬環境：
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install pillow requests
   ```

## 🔒 安全規則與隱私防護
請遵循 [ANTIGRAVITY.md](file:///d:/antigravity/2026ppt-by-notebooklm/ANTIGRAVITY.md) 的安全設定。請勿將個人 API 金鑰、OAuth 憑證或 `notebooks.json` 提交至公開 GitHub 儲存庫。
