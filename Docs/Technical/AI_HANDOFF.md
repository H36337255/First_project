# AI Development Handoff

本文件供後續 GPT／Codex 或其他開發代理接手專案時使用。

## 開始工作前

1. 完整閱讀根目錄 `README.md`。
2. 閱讀 `Docs/Production/DECISIONS.md`，遵守 Accepted 決策。
3. 檢查 `Docs/Production/Milestones.md` 與目前分支狀態。
4. 新增或修改美術資產前更新 `AssetRegistry.csv`。
5. 不得在未記錄決策的情況下更換 Unity、渲染管線或多人框架。

## 工程限制

- 鎖定 Unity 6.3 LTS，除非新增決策明確升級。
- MVP 使用 GameObject／MonoBehaviour 工作流，不導入 DOTS／Netcode for Entities。
- 房主權威判定任務、分數、貨幣、事件和重要物理結果。
- 純視覺碎片與粒子不做網路同步。
- 新增第三方套件前，先說明用途、授權、替代方案和維護風險。
- 不將祕密、金鑰、Steam App 憑證或本機設定提交到 Git。
- 不修改其他功能的檔案來順便重構；每個 Commit 保持單一目的。

## 完成一項工作的最低要求

- 專案可編譯，沒有新增錯誤。
- 核心邏輯具有適當 EditMode 或 PlayMode 測試。
- 多人功能至少測試 Host 加一名 Client。
- 重要 Inspector 欄位有 Tooltip 或文件。
- 新資產符合 README 命名規則並登記 AssetID。
- 更新 Milestones 或 Decisions 中受影響的項目。

## 建議回報格式

```text
Outcome:
Changed:
Verified:
Known risks:
Next smallest step:
```
