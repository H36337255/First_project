# Wedding Mayhem Agent Instructions

本指令適用於整個 Repository，供 Codex、GPT 或其他程式開發代理使用。

## 工作前必讀

依序閱讀：

1. `README.md`
2. `Docs/Production/DECISIONS.md`
3. `Docs/Production/Milestones.md`
4. `Docs/Production/AssetRegistry.csv`
5. `Docs/Technical/AI_HANDOFF.md`
6. 本次指定的工作單

若工作要求與 `DECISIONS.md` 中的 Accepted 決策衝突，先停止並提出決策變更，不得自行推翻。

## 專案基線

- 類型：2–6 人第一人稱合作喜劇。
- 地圖：戶外露天花園婚禮。
- 引擎：Unity 6.3 LTS、URP、C#。
- 多人：Netcode for GameObjects；房主權威。
- 主要測試人數：4 人；最低 2 人；架構上限 6 人。
- 博弈：僅限單局婚禮幣、押注倍率和分數，不得交易或連結真實貨幣。
- 合作：共享主要目標，加上不致命的個人秘密任務。

## 實作規則

- 程式、檔名、命名空間及 Inspector 欄位使用英文。
- 說明文件及面向使用者的企劃預設使用繁體中文。
- C# 使用 `WeddingMayhem` 根命名空間。
- 優先建立小型、可測試、單一職責的元件。
- 遊戲規則不得直接寫死在 Scene；可調內容使用 ScriptableObject。
- 任務、分數、貨幣、事件和關鍵物理結果由 Host 判定。
- 純視覺碎片、粒子和非關鍵布料效果不做網路同步。
- 不加入未經核准的付費資產、閉源套件或需要持續付費的服務。
- 不手動編造 Unity `.meta` GUID；讓指定 Unity Editor 建立及維護。
- 新增美術或音效資產前，先更新 `AssetRegistry.csv`。
- 不提交 Unity `Library/`、`Temp/`、`Logs/`、`Obj/` 或建置輸出。
- 未實際執行的測試必須明確標記為未驗證，不得聲稱通過。

## 變更與 Git

- 每次只處理一份工作單，避免同時實作多個里程碑。
- 使用 `feature/<name>` 或 `asset/<name>` 分支。
- Commit 遵循 `feat:`、`fix:`、`art:`、`net:`、`test:`、`docs:` 前綴。
- 保留使用者既有修改，不做破壞性重設或無關重構。
- 完成後提供變更摘要、驗證結果、已知風險與下一個最小步驟。

## 完成定義

- Unity 專案能以指定版本開啟且沒有新增編譯錯誤。
- 核心邏輯具備適當的 EditMode 或 PlayMode 測試。
- 多人行為至少以 Host 加一名 Client 驗證。
- 重要 Inspector 欄位具備 Tooltip 或對應文件。
- 目錄、命名與資產 ID 符合 README。
- 相關 Milestone、Decision 或 Asset Registry 已同步更新。
