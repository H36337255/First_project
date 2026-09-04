# Codex Work Package 001

## 任務名稱

建立 Unity 專案基線與第一人稱互動垂直切片。

## Repository

- URL：`https://github.com/H36337255/First_project`
- 建議分支：`feature/phase-1-interaction`
- 基礎分支：`main`

## 執行目標

將現有企劃 Repository 初始化為 Unity 6.3 LTS URP 專案，完成一個可在本機操作的第一人稱 Interaction Lab。此工作單只處理單機互動基線，不實作 Lobby、Relay、完整婚禮關卡、NPC 或押注系統。

## 開始前

1. 完整閱讀根目錄 `AGENTS.md` 及其列出的文件。
2. 檢查目前分支與工作樹，保留既有內容。
3. 確認環境可使用 Unity 6.3 LTS；採用已安裝的最新 6.3 LTS patch，不猜測版本號。
4. 如果環境沒有 Unity Editor，仍可完成不依賴 Editor 的安全文件或 C# 工作，但不得手寫 Scene、Prefab 或 `.meta` 來假裝已驗證；清楚列出阻礙。

## 必須交付

### A. Unity 基線

- 建立或確認 Unity 6.3 LTS URP 專案。
- 啟用 Visible Meta Files 與 Force Text。
- 安裝與版本相容的 Input System。
- 保留既有 `Assets/WeddingMayhem/` 架構。
- 建立必要 Assembly Definition，至少分離 Runtime 與 Tests。
- 不在此工作單加入付費或非必要第三方套件。

### B. 第一人稱控制

- WASD 移動。
- 滑鼠視角。
- 可設定移動速度與滑鼠靈敏度。
- 遊戲時鎖定游標，Escape 可釋放游標。
- 使用 CharacterController 或同等簡潔方案；選擇需寫入技術說明。

### C. 通用互動系統

- 建立 `IInteractable` 或等效介面。
- 從玩家攝影機進行可設定距離的互動偵測。
- 提供目前目標與提示文字資料，不讓 UI 直接依賴特定物件類別。
- Input System 的 Interact action 預設綁定 `E`。
- 互動邏輯與輸入讀取分離，方便後續網路化。

### D. 可搬運物件

- 建立具有 Rigidbody 的 `GrabbableObject`。
- 玩家可以拿起、保持、放下與丟出測試物件。
- 可設定重量、持有距離、丟擲力量與是否易碎。
- 避免以 Transform 瞬移造成明顯穿模或無限物理力量。
- 本工作單只做單機版，但 API 必須保留後續 Host 權威化空間。

### E. Interaction Lab

- 透過 Unity Editor 建立 `SCN_91_InteractionLab`。
- 使用簡單 Primitive 建立地板、桌面、坡道與障礙。
- 至少放入三個不同重量的搬運物件。
- 放入一個蛋糕替代物，驗證脆弱物件掉落或碰撞狀態。
- 不投入正式美術，不提前製作戶外婚禮完整地圖。

### F. 測試與文件

- 為不依賴畫面的核心互動狀態撰寫 EditMode 測試。
- 若可使用 Unity Test Runner，執行相關測試並記錄結果。
- 更新 `Docs/Production/Milestones.md`。
- 新增 `Docs/Technical/INTERACTION_ARCHITECTURE.md`，說明控制器、偵測、抓取與未來網路化邊界。
- 若新增暫代資產，更新 `AssetRegistry.csv` 或明確標記為開發用 Primitive。

## 驗收條件

- [ ] Unity 6.3 LTS 能開啟專案且 Console 無編譯錯誤。
- [ ] 玩家能在 Interaction Lab 移動與環視。
- [ ] `E` 可與目前瞄準的物件互動。
- [ ] 玩家能拿起、放下與丟出三種重量物件。
- [ ] 蛋糕替代物可進入完整／受損狀態。
- [ ] 互動距離、移動速度、靈敏度與丟擲力量可設定。
- [ ] 核心測試通過，或清楚列出未能執行的原因。
- [ ] README、Decision 與既有企劃規則未被無理由改寫。
- [ ] 沒有提交 Unity 快取、建置輸出或敏感資料。

## 明確排除

- 不實作線上多人連線。
- 不實作 Steamworks。
- 不實作正式 NPC。
- 不實作婚禮幣與押注 UI。
- 不製作完整花園婚禮地圖。
- 不購買或下載付費 Asset Store 資產。
- 不把全部 12 週里程碑塞進本次工作。

## Codex 回報格式

```text
Outcome:
Changed:
Verified:
Unverified or blocked:
Known risks:
Next smallest step:
```

## 可直接交給 Codex 的提示詞

```text
請執行 Repository 根目錄 CODEX_TASK.md 的 Work Package 001。

開始前完整閱讀 AGENTS.md 及其要求的文件。使用 feature/phase-1-interaction 分支，保留既有內容，只完成 Unity 6.3 LTS 專案基線、第一人稱控制、通用互動、可搬運物件、Interaction Lab 與對應測試。不要提前實作多人連線、Steamworks、NPC、押注系統或完整婚禮地圖。

若執行環境沒有 Unity Editor，不要手寫 Scene、Prefab 或 .meta 冒充完成；完成能安全完成的部分，列出精確阻礙與使用者下一步。最後依 CODEX_TASK.md 指定格式回報。
```
