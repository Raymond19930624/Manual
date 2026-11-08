# Prism Manuals (設備說明書總匯)

> 個人電器與 3C 數位設備說明書總匯｜採用 **Apple Support 極簡空氣感** 設計語言，無廣告、無多餘浮誇元素，電腦與手機皆具備極致閱讀體驗。

- **線上網址**：[https://manual.prismoment.com](https://manual.prismoment.com)
- **主機託管**：Cloudflare Pages / Workers
- **收錄設備數**：18 款手冊深度還原（包含硬體圖解、操作步驟、完整故障代碼表、原廠 PDF 內嵌與下載）

---

## 收錄設備一覽

1. **Godox C01** 微型無線麥克風
2. **Anker Prime 160W (A2687)** 多口氮化鎵快充
3. **綠聯 160W (X774)** 五口氮化鎵快充
4. **GAME’NIR ProX-Legend7Ds** 雙震動電玩手把
5. **Panasonic KZ-PH34-K** 智慧 IH 電磁爐
6. **SUNLU S4** 四槽 3D 列印耗材乾燥箱
7. **飛利浦 / 特福** 鮮呼吸智能萬用壓力鍋
8. **Panasonic NN-ST34H** 25L 微電腦微波爐
9. **伊萊克斯 EDH10TRBW1** 10L 清淨除濕機
10. **VIOMI 雲米 WD10FT-B6T** 10KG 變頻洗脫烘洗衣機
11. **CITIZEN BZ1040 / W770** 藍牙光動能腕錶
12. **SEIKO SSC 系列 (V172)** 太陽能計時碼錶
13. **快譯通 S86** 星光夜視電子後視鏡行車記錄器
14. **Nitecore D4** 四槽液晶多功能智能充電器
15. **綠林** 數顯可調溫便攜電烙鐵
16. **Kolin 歌林 KNJ-LN102P** 多功能隨行美食鍋
17. **AOC 70U6418/96T** 70吋 4K 智慧顯示器
18. **TP-Link Deco X55** AX3000 Mesh Wi-Fi 6 系統

---

## 專案結構

```text
Manual/
├── index.html                   # 總匯首頁（全域搜尋、類別篩選、深淺色切換）
├── CNAME                        # manual.prismoment.com
├── wrangler.jsonc               # Cloudflare Workers/Pages 靜態資源配置
├── assets/                      # 共用樣式與字體
└── devices/                     # 18 款設備獨立手冊
    ├── godox-c01/               # 互動手冊 + 原圖
    ├── anker-prime-160w/        # 互動手冊 + original.pdf
    └── ... (其餘設備目錄)
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
