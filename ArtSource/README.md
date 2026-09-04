# ArtSource

此資料夾保存可編輯的美術來源檔，不讓 Unity 直接引用。

```text
ArtSource/
├─ Blender/
│  ├─ Environment/
│  ├─ Props/
│  ├─ Characters/
│  └─ Vehicles/
├─ Textures/
├─ AudioSessions/
├─ References/
└─ Exports/
```

## 工作規則

1. 建模前先在 `Docs/Production/AssetRegistry.csv` 登記 AssetID。
2. Blender 原檔使用 `AssetID_Name.blend` 命名。
3. 模型先完成 Blockout 並在 Unity 驗證比例，再製作細節。
4. FBX 與貼圖匯出後放入 `Assets/WeddingMayhem/Art/` 對應分類。
5. 每個外部參考與第三方素材需記錄來源和授權。
6. 不使用 `final`、`new` 或 `copy` 當作版本名稱；版本由 Git 管理。
