# Wedding Mayhem（暫定名稱）

一款以戶外露天婚禮為舞台的 2–6 人第一人稱合作喜劇遊戲。玩家是臨時組成的婚禮救火團隊，必須在有限時間與預算內完成儀式，同時處理天氣、賓客、供應商與朋友造成的連鎖災難。

> 專案狀態：前期企劃／原型準備  
> 目標平台：Windows、Steam  
> 開發規模：單人，3–6 個月  
> 暫定引擎：Unity 6.3 LTS、URP、C#  
> 連線人數：2–6 人，以 4 人作為主要平衡與測試基準

## 1. 遊戲定位

### 一句話提案

和朋友合力救回一場不斷失控的露天婚禮，拿本局賺到的婚禮幣押注更困難的任務，在完美謝幕或全面翻車之前決定是否收手。

### 設計支柱

1. **合作本身就是笑點**：搬運、交接、溝通和誤會都能產生意外。
2. **失敗仍然有娛樂性**：事故不只扣分，也會開啟新的補救方法與荒謬場面。
3. **風險由玩家選擇**：玩家自行押注高風險目標，不以純隨機決定勝負。
4. **短時間完成一局**：目標每局 20–30 分鐘，10 分鐘內也能完成原型測試。
5. **適合直播與短影音**：每局應自然產生明確、可理解、可剪輯的翻車瞬間。

### 不做的內容

- 不使用真實貨幣下注。
- 不允許婚禮幣交易、兌現或購買。
- 不以付費抽獎影響能力或分數。
- MVP 不製作大型開放世界、專用伺服器或複雜婚禮編輯器。
- MVP 不製作真正破壞全隊目標的隱藏叛徒。

## 2. 核心遊戲循環

1. **接案**：選擇婚禮合約、基本難度、天氣預報與可選挑戰。
2. **籌備**：使用有限預算選擇供應商、保險與緊急工具。
3. **押注**：使用本局婚禮幣接受公開團隊賭注或個人秘密任務。
4. **進場**：分配工作，將蛋糕、戒指、酒水、椅子與設備送到正確位置。
5. **儀式**：按照流程處理賓客、主持、攝影、音響及突發事件。
6. **加碼或收手**：在流程節點提高倍率，或提前鎖定部分分數。
7. **結算**：依完成度、賓客滿意、事故、時間、預算與押注倍率計分。

### 單局貨幣與風險押注

- 每局開始提供固定基礎婚禮幣，結束後歸零。
- 完成工作、快速救場和取悅賓客可獲得婚禮幣。
- 婚禮幣可用於押注、緊急服務、保險或臨時升級。
- 高賠率挑戰範例：蛋糕零損傷、全員準時入席、停電時仍完成致詞。
- 每個關鍵流程提供一次「結算／加碼」選擇。
- 隨機事件只改變局勢；成功與否主要由操作、判斷及合作決定。
- 局外獎勵限於服裝、表情、名牌和裝飾，不提供數值優勢。

### 合作與秘密任務

全隊共享主要婚禮目標。每名玩家另外取得一個不致命的秘密任務，例如：

- 讓三位賓客改喝香檳。
- 在不打斷儀式的前提下與每位隊友擊掌。
- 讓特定賓客出現在三張團體照中。
- 保持某張桌面全程沒有空杯。

秘密任務只能影響額外分數，不得要求玩家蓄意讓婚禮失敗。

## 3. 第一張地圖：戶外花園婚禮

### 地圖區域

| 區域 ID | 區域 | 主要玩法 | 主要資產 |
|---|---|---|---|
| Z01 | 入口與停車區 | 接貨、引導賓客、婚車事件 | 拱門、指示牌、車輛、禮物桌 |
| Z02 | 儀式草坪 | 座位、紅毯、戒指、誓詞 | 椅子、花道、證婚台、花藝 |
| Z03 | 雞尾酒區 | 酒水、點心、賓客社交 | 高腳桌、吧台、杯具、遮陽傘 |
| Z04 | 宴會帳篷 | 上菜、致詞、蛋糕、舞池 | 圓桌、舞台、蛋糕桌、音響 |
| Z05 | 後台服務區 | 補貨、修理、供電、垃圾處理 | 貨架、冰箱、工具、垃圾桶 |
| Z06 | 花園與水景 | 拍照、尋物、風雨事故 | 樹木、灌木、水池、拍照背板 |
| Z07 | 設備與供電區 | 發電機、燈串、灑水與電纜 | 發電機、配電箱、電纜、灑水器 |

### 首批事件

- 陣風掀翻桌布、花藝或指示牌。
- 突然降雨，玩家需展開帳篷並保護音響。
- 灑水器誤啟，導致賓客、地面和電纜出現問題。
- 蛋糕車延誤，玩家必須以替代甜點救場。
- 戒指掉入草地、水池或賓客禮物堆。
- 喝醉的賓客搶走麥克風或走上紅毯。
- 小孩追逐花童、氣球或蛋糕裝飾。
- 發電機過載，使燈光、音樂和冷藏設備互相爭奪電力。

## 4. 技術方案

### 暫定技術棧

- Unity 6.3 LTS
- Universal Render Pipeline（URP）
- C#
- Input System
- Netcode for GameObjects
- Multiplayer Services SDK：Lobby、Relay、Session
- Git、Git LFS
- Blender：3D 來源模型
- Krita、Photoshop 或同類工具：貼圖來源檔

### 多人同步原則

- 採 **Host authoritative**：房主判定任務、分數、貨幣、事件與重要物理結果。
- 任務物件才同步，例如蛋糕、戒指、酒瓶、麥克風和發電機。
- 純視覺碎片與粒子只在本機產生，例如碎盤、彩帶、雨滴和酒水飛濺。
- NPC 同步狀態與目標，不逐幀同步完整動畫。
- 角色布料和完整 Ragdoll 不列入 MVP 的精確網路同步。
- 原型支援 6 人連線，但效能與玩法以 4 人作為標準測試情境。

### 場景載入

- `Bootstrap` 常駐，負責服務初始化、設定與場景切換。
- `MainMenu`、`Lobby` 與婚禮關卡分離。
- 婚禮關卡拆成 Lighting、Environment、Gameplay、Navigation 等可加載子場景。
- 測試場景與正式場景分離，禁止在正式地圖測試未完成系統。

## 5. Repository 資料架構

```text
WeddingMayhem/
├─ README.md
├─ LICENSE
├─ .gitignore
├─ .gitattributes
├─ ArtSource/
│  ├─ Blender/
│  │  ├─ Environment/
│  │  ├─ Props/
│  │  ├─ Characters/
│  │  └─ Vehicles/
│  ├─ Textures/
│  ├─ AudioSessions/
│  ├─ References/
│  └─ Exports/
├─ Assets/
│  └─ WeddingMayhem/
│     ├─ Art/
│     │  ├─ Animations/
│     │  ├─ Characters/
│     │  ├─ Environment/
│     │  │  └─ GardenWedding/
│     │  ├─ Materials/
│     │  ├─ Models/
│     │  │  ├─ Architecture/
│     │  │  ├─ Furniture/
│     │  │  ├─ GameplayProps/
│     │  │  ├─ Nature/
│     │  │  └─ Vehicles/
│     │  ├─ Textures/
│     │  ├─ VFX/
│     │  └─ UI/
│     ├─ Audio/
│     │  ├─ Ambience/
│     │  ├─ Music/
│     │  ├─ SFX/
│     │  └─ Voice/
│     ├─ Data/
│     │  ├─ Bets/
│     │  ├─ Events/
│     │  ├─ Guests/
│     │  ├─ Items/
│     │  ├─ Maps/
│     │  ├─ RoundConfigs/
│     │  ├─ ScoreRules/
│     │  ├─ SecretObjectives/
│     │  ├─ Tasks/
│     │  └─ Vendors/
│     ├─ Localization/
│     ├─ Networking/
│     │  ├─ Prefabs/
│     │  ├─ Runtime/
│     │  └─ Tests/
│     ├─ Prefabs/
│     │  ├─ Characters/
│     │  ├─ Environment/
│     │  ├─ Gameplay/
│     │  ├─ Networked/
│     │  └─ UI/
│     ├─ Scenes/
│     │  ├─ Core/
│     │  ├─ Maps/
│     │  │  └─ GardenWedding/
│     │  └─ Tests/
│     ├─ Scripts/
│     │  ├─ Core/
│     │  ├─ Gameplay/
│     │  ├─ Interaction/
│     │  ├─ Networking/
│     │  ├─ NPC/
│     │  ├─ Scoring/
│     │  ├─ UI/
│     │  └─ Utilities/
│     ├─ Settings/
│     └─ Tests/
│        ├─ EditMode/
│        └─ PlayMode/
├─ Docs/
│  ├─ Design/
│  ├─ Production/
│  │  ├─ AssetRegistry.csv
│  │  └─ Milestones.md
│  ├─ Technical/
│  └─ References/
├─ Packages/
└─ ProjectSettings/
```

### 資料夾規則

- `ArtSource/`：Blender、PSD、Krita、DAW 工程等可編輯來源檔。
- `Assets/WeddingMayhem/`：Unity 實際使用的匯出資產與程式。
- 第三方套件不得混入 `WeddingMayhem/`；保留原始供應商資料夾與授權文件。
- `References/` 只放有來源、授權或連結紀錄的參考資料。
- 每個 Unity 資產必須保留 `.meta`，並啟用 Visible Meta Files 與 Force Text。
- 大型二進位檔使用 Git LFS，不直接把快取或建置結果提交到 Git。

## 6. Unity 場景架構

```text
Scenes/
├─ Core/
│  ├─ SCN_00_Bootstrap.unity
│  ├─ SCN_01_MainMenu.unity
│  └─ SCN_02_Lobby.unity
├─ Maps/GardenWedding/
│  ├─ SCN_10_GardenWedding_Blockout.unity
│  ├─ SCN_11_GardenWedding_Master.unity
│  ├─ SCN_11A_GardenWedding_Environment.unity
│  ├─ SCN_11B_GardenWedding_Gameplay.unity
│  ├─ SCN_11C_GardenWedding_Lighting.unity
│  └─ SCN_11D_GardenWedding_Navigation.unity
└─ Tests/
   ├─ SCN_90_NetworkTest.unity
   ├─ SCN_91_InteractionLab.unity
   └─ SCN_92_PhysicsLab.unity
```

`SCN_11_GardenWedding_Master` 只管理子場景與載入，不直接堆放模型。這可讓場景美術、玩法物件、光照與導航分開修改。

## 7. 資料驅動設計

玩法內容使用 ScriptableObject 定義，避免把數字與事件寫死在場景或程式中。

| 資料類型 | 建議類別 | 用途 |
|---|---|---|
| 地圖 | `MapDefinition` | 地圖場景、區域、容量與事件池 |
| 單局設定 | `RoundConfig` | 時間、初始幣、難度、玩家倍率 |
| 工作 | `TaskDefinition` | 條件、階段、時間、獎勵與失敗結果 |
| 隨機事件 | `EventDefinition` | 觸發條件、權重、互斥與後續事件 |
| 團隊押注 | `BetDefinition` | 成本、倍率、成功與提前結算條件 |
| 秘密任務 | `SecretObjectiveDefinition` | 個人條件、可見性與額外分數 |
| 物件 | `ItemDefinition` | 重量、抓取方式、價值、破損狀態 |
| 賓客 | `GuestArchetype` | 個性、需求、耐心、事故傾向 |
| 供應商 | `VendorDefinition` | 價格、可靠度、風險與替代方案 |
| 計分 | `ScoreRuleSet` | 星級、時間、事故與倍率計算 |

所有定義使用穩定 ID，例如 `EVT_WEATHER_GUST_001`，存檔和網路訊息不得依賴顯示名稱。

## 8. 資產命名規則

格式：`類型_主題_名稱_變體_版本`

| 前綴 | 資產 | 範例 |
|---|---|---|
| `SCN_` | Scene | `SCN_11_GardenWedding_Master` |
| `MDL_` | 3D 模型 | `MDL_Wedding_FoldingChair_A` |
| `SKM_` | 骨架模型 | `SKM_Guest_Adult_A` |
| `AN_` | 動畫 | `AN_Guest_Clap_Loop` |
| `PF_` | Prefab | `PF_Prop_WeddingCake_A` |
| `NPF_` | 網路 Prefab | `NPF_Item_RingBox_A` |
| `MAT_` | 材質 | `MAT_Fabric_Tablecloth_White` |
| `T_` | 貼圖 | `T_Tablecloth_BaseColor_2K` |
| `SFX_` | 音效 | `SFX_Glass_Break_01` |
| `AMB_` | 環境音 | `AMB_GardenWedding_Day` |
| `VFX_` | 特效 | `VFX_ConfettiBurst_A` |
| `SO_` | ScriptableObject | `SO_Bet_CakeNoDamage` |
| `UI_` | UI 資產 | `UI_Icon_WeddingCoin` |

規則：

- 檔名、資料夾、程式類別一律使用英文與 ASCII。
- 不使用空白、中文、`final`、`new`、`copy` 等不可追蹤版本字樣。
- 變體用 `A/B/C`；真正版本由 Git 管理，不建立 `v2_final_final`。
- 貼圖後綴固定為 `BaseColor`、`Normal`、`Mask`、`Emission`。

## 9. 3D 建模與 Prefab 流程

### 資產生命週期

```text
Requested → Reference → Blockout → Modeling → UV → Texture
→ Collision/LOD → Exported → Prefab → Integrated → QA → Approved
```

禁止跳過 `Blockout` 直接製作精細模型。必須先確認比例、操作空間與網路碰撞需求。

### 模型交付標準

- 單位：1 Unity unit = 1 公尺。
- Up 軸與 Export 設定需全專案一致。
- Pivot 放在實際抓取、旋轉或落地所需的位置。
- 可搬運物品使用簡化 Collider，不以高面數 Mesh Collider 作為預設。
- 靜態建築、帳篷和大型家具需規劃 LOD；小型手持物可暫不製作 LOD。
- 材質槽數量保持最低，同一組婚宴資產優先共用材質與貼圖集。
- 每個模型需有比例參考、正確命名、Prefab、Collider 與預覽圖。
- 網路互動物件必須經過 2 人與 6 人連線測試後才能標記 Approved。

### 資產登錄表欄位

`Docs/Production/AssetRegistry.csv` 預計使用以下欄位：

| 欄位 | 說明 |
|---|---|
| `AssetID` | 永久唯一 ID，例如 `PROP_CAKE_001` |
| `Category` | Environment、Prop、Character、VFX、Audio、UI |
| `Name` | 人類可讀名稱 |
| `MapOrSystem` | 所屬地圖或系統 |
| `Priority` | Must、Should、Could |
| `Status` | 資產生命週期狀態 |
| `SourcePath` | Blender／貼圖來源路徑 |
| `UnityPath` | Unity 匯出資產路徑 |
| `PolyBudget` | 建議面數預算 |
| `TextureSet` | 共用貼圖集名稱與解析度 |
| `LOD` | LOD 數量或 N/A |
| `Collider` | Box、Capsule、Convex、Compound 等 |
| `Networked` | Yes／No |
| `Reusable` | 是否可跨地圖使用 |
| `License` | 自製或第三方授權來源 |
| `Notes` | 阻礙、依賴與修改紀錄 |

## 10. 戶外婚禮資產拆分

### MVP 必須資產（Must）

- 模組化草地、地面與石板路。
- 儀式拱門、花道、折疊椅、圓桌與宴會帳篷。
- 蛋糕、蛋糕推車、戒指盒、捧花、酒瓶、酒杯、餐盤、麥克風。
- 發電機、電纜、配電箱、音響與燈串。
- 玩家角色基本身體與 3–4 組顏色變體。
- 賓客角色模組：身體、髮型、服裝、膚色和配件。
- 雨、風、紙花、破碎與酒水飛濺特效。
- 基本圖示、任務提示、押注卡片與結算畫面。

### 第二階段資產（Should）

- 婚車、停車區與送貨車。
- 水池、花園雕像、拍照背板與大型花藝。
- 兒童、長者與特殊賓客變體。
- 自助餐、雞尾酒吧及更多食物。
- 遮陽傘、雨傘、臨時帳棚與救場工具。

### 延後資產（Could）

- 高精度布料模擬。
- 可完全破壞的帳篷或建築。
- 大量可駕駛車輛。
- 完整角色捏臉與服裝編輯器。
- 台灣辦桌婚禮地圖與文化事件包。

## 11. Git 與版本管理

### 分支

- `main`：隨時可開啟與測試的穩定版本。
- `feature/<name>`：單一玩法或系統。
- `asset/<name>`：較大型的模型、場景或美術整合。
- 小型單人專案暫不建立長期 `develop` 分支，以降低合併成本。

### Git LFS

建議納入 LFS：

```text
*.fbx
*.blend
*.psd
*.kra
*.wav
*.mp3
*.ogg
*.png
*.tga
*.exr
*.unitypackage
```

不提交：`Library/`、`Temp/`、`Logs/`、`Obj/`、`Build/`、IDE 快取及本機使用者設定。

### Commit 格式

```text
feat: add cake delivery task
fix: prevent duplicate wedding coin payout
art: add ceremony chair variants
net: sync ring box ownership
docs: update asset naming rules
```

## 12. 12 週原型里程碑

| 週期 | 交付目標 |
|---|---|
| 1–2 | 第一人稱移動、抓取、搬運、互動測試場 |
| 3–4 | Host／Join、2–6 人加入、重要物件同步 |
| 5–6 | 戶外婚禮灰盒、蛋糕與戒指兩條任務鏈 |
| 7–8 | 分數、婚禮幣、押注、提前結算、秘密任務 |
| 9–10 | 風雨、供電、賓客事件與第一輪替換美術 |
| 11 | 4 人與 6 人測試、效能、同步與斷線修正 |
| 12 | 10–20 分鐘公開原型、預告片素材與回饋表 |

若核心循環通過測試，再用剩餘時間增加事件、資產品質、Steam 整合及新手引導。

## 13. MVP 驗收條件

- 2–6 名玩家能透過邀請碼加入同一局。
- 玩家可以抓取、搬運、交接與破壞關鍵婚禮物品。
- 完整完成一場 10–20 分鐘戶外婚禮。
- 至少有 3 條主要任務鏈與 8 種突發事件。
- 至少有 6 種團隊押注與 8 種個人秘密任務。
- 分數、婚禮幣與押注結果皆由房主正確判定。
- 4 人標準測試中，每局能自然產生至少 3 次可理解的翻車或救場時刻。
- 玩家即使輸掉分數，仍能理解失敗原因並願意立刻再玩一局。

## 14. 待確認事項

- 正式遊戲名稱。
- 美術方向：低多邊形、卡通比例或半寫實。
- 玩家角色設定：婚禮工作人員、親友救火隊或兩者混合。
- 是否在 MVP 加入近距離語音，或第一階段只使用外部語音測試。
- GitHub Repository 網址與預設分支。
- 是否採用免費／付費 Asset Store 資產，以及單項與總預算。

## 15. 後續文件

Repository 建立後，依需要再從本文件拆出：

- `Docs/Design/GAME_DESIGN.md`
- `Docs/Technical/NETWORK_ARCHITECTURE.md`
- `Docs/Production/AssetRegistry.csv`
- `Docs/Production/Milestones.md`
- `Docs/Production/DECISIONS.md`
- `Docs/Technical/AI_HANDOFF.md`

`README.md` 保持為專案入口；細節移入上述文件後，README 只保留摘要與連結。
