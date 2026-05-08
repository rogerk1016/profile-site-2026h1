# Profile Site · 2026 H1 工作報告

> 個人 2026 年上半年工作回顧網頁,以單頁(SPA)形式呈現專案成果、AI 協作方法、Roadmap 與反思。

- **作者**:Roger Chen (MAKALOT MIS · ERP Application Developer)
- **期別**:2026 H1 (Annual Review · 5 月簡報用)
- **報告對象**:處長 / 主管階層
- **形式**:單一 HTML 檔案,搭配 `assets/` 內的截圖

---

## 專案目的

把 H1 的關鍵專案、AI 協作辦法、效能優化成果、Roadmap 統一在一頁網頁中呈現,作為向處長的 H1 工作報告載體。重點:

- 用視覺化排版取代純文字 / PPT,讓處長 5 分鐘內掌握全貌
- 量化成果:完成率、AI 協作比例、工時節省、效能提升
- 用 8 個關鍵專案串起 PO / AP / GL / COST / D2K Form / RPA / VBA 的工作軸
- 強調「Coder → Reviewer」的角色轉變與 AI 協作辦法 (11 步開發實錄)

---

## 主要章節

| 章節 | 內容 |
|---|---|
| **HELLO** | 自我介紹 + 角色 / 方法 / 領域 / H1 最愛專案 |
| **OVERVIEW** | 27 件總工作 · 85.2% 完成率 · 22.2% AI 協作比例(可 hover 看 H2 預期) |
| **PROJECTS** | 8 個 H1 專案:採購合約、產區副料簽核、主副料拋帳平台、越南海關修改、BGD AP→GL、PR BY CPO 效能優化、實際成本改版、商品存貨 |
| **METHODOLOGY** | Coder → Reviewer 的 AI 協作辦法、11 步開發實錄、4 種協作場景對話 |
| **ROADMAP** | H2 6 個里程碑(進行中 / 規劃中 / TBD) |
| **REFLECTIONS** | 三點反思:AI 協作雙價值、規格完整度比工時更值錢 |
| **OTHERS** | 其他維護工作 |

---

## 技術棧

| 項目 | 採用 |
|---|---|
| HTML | 原生 HTML5,單一 `index.html`(約 1,640 行) |
| CSS | Tailwind CSS v3 (CDN script + `tailwind.config` inline) |
| Fonts | Inter + Noto Sans TC + JetBrains Mono(Google Fonts CDN) |
| 互動 | 原生 JavaScript:scroll progress bar + IntersectionObserver reveal + active nav |
| 字型 / 配色 | 自訂 Tailwind palette(navy / gold / cyan2 / coral / forest / royal …) |

**沒有 build step** — 直接用瀏覽器開 `index.html` 即可預覽,也可直接放到任何 static hosting (GitHub Pages、Netlify 等)。

---

## 目錄結構

```
profile_site/
├── index.html       # 單一頁面,所有章節都在這
├── README.md        # 本檔
├── .gitignore
└── assets/          # 專案截圖
    ├── img2.jpg     ~ img36.jpg (16 張)
    └── ...
```

---

## 字體可讀性設計

考量處長閱讀年齡(50+),全站字級採:

- **Body 內容**:≥ 14px
- **小標籤 / kicker**:≥ 12px
- **數字 / 標題**:依層級 17 ~ 120 px

整站經過字級 +2px 通盤升級,確保正常閱讀距離(30~40 cm)無需瞇眼。

---

## 本地預覽

```bash
# 方式 1:直接用瀏覽器開
open index.html             # macOS
start index.html            # Windows
xdg-open index.html         # Linux

# 方式 2:用 Python 起 local server (避免 file:// 限制)
python -m http.server 8000
# 開瀏覽器到 http://localhost:8000
```

---

## 設計原則(內部備忘)

1. **不過度使用 emoji** — 處長偏好乾淨文字
2. **句號後換行** — 中文長句用 `<br>` 強制斷行,提升可讀性
3. **顏色語意統一** — 藍 = 人類 / 橘紅 = AI / 綠 = 完成 / 灰 = 待調整
4. **避免單純圖片** — 截圖內如有重要文字,優先轉 HTML 排版以保可讀性

---

## Remote

| | URL |
|---|---|
| GitHub (private) | https://github.com/rogerk1016/profile-site-2026h1 |
