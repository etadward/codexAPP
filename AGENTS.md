# Repository Instructions

請用繁體中文回覆。
先給結論，再補充原因。
回答盡量簡潔、實用。

## Git 同步規則

- 開始處理這個 repo 前，先檢查目前 branch、工作區狀態與遠端同步狀態。
- 如果工作區乾淨，先執行 `git pull --ff-only`，再開始修改。
- 如果工作區有未提交變更，不要直接 pull；先向使用者說明狀態並確認下一步。
- 完成可提交的變更後，建立 commit，並在使用者要求或任務明確需要跨電腦同步時執行 `git push`。
- 不要提交 `.codex/local/`、`.codex/tmp/`、API key、token、密碼或任何機器專屬設定。

## 路徑規則

- 優先使用 repo 相對路徑。
- 不要把 `C:\Users\...` 這類本機絕對路徑寫進共用檔案。
- 每台電腦不同的設定放在 `.codex/local/`，且不得提交。
