# Prism Manuals (設備說明書總匯)

> 專為個人手邊各類電器、攝影影音與數位設備打造的數位說明書總匯。  
> 採用 **Apple Support 極簡空氣感** 設計語言，無廣告、無多餘浮誇元素，電腦與手機皆具備極致閱讀體驗。

- **線上網址**：https://manual.prismoment.com
- **主機託管**：Cloudflare Pages / GitHub Pages

---

## 專案結構

```text
Manual/
├── index.html                   # 總匯首頁（全域搜尋、類別篩選）
├── CNAME                        # manual.prismoment.com
├── .gitignore
├── README.md
└── devices/                     # 各設備獨立手冊
    └── godox-c01/               # Godox C01 無線麥克風
        ├── index.html           # 互動說明書
        └── godox-c01-manual-original.jpg
```

---

## 如何新增下一台設備？

1. 在 `devices/` 目錄下建立新設備資料夾（例如 `devices/sony-zv-e10/` 或 `devices/coffee-machine/`）。
2. 在該資料夾放入設備說明書 `index.html` 與相關圖片。
3. 在根目錄 `index.html` 的 `#devicesGrid` 區塊加入對應的卡片即可！

---

## 部署至 Cloudflare Pages

1. 登入 [Cloudflare Dashboard](https://dash.cloudflare.com/) ➔ **Workers & Pages** ➔ **Create application** ➔ **Pages** ➔ **Connect to Git**。
2. 選擇此儲存庫 `Raymond19930624/Manual`。
3. 設定：
   - **Framework preset**：`None`
   - **Build output directory**：`/`（根目錄）
4. 點擊 **Save and Deploy**。
5. 在 Pages 專案的 **Custom domains** 頁籤新增自訂網域：`manual.prismoment.com`。
   - 因為 `prismoment.com` 已經在 Cloudflare 託管，系統會自動添加 DNS 記錄，無需任何手動設定！
