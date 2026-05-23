# SEO 實戰執行路線圖

> Tailor-made for hands-on practitioners who have SEO concept but lack execution confidence.
> 適合有概念但需要「坐低就做到」嘅實戰路線。

---

## 你的 Profile（起點）

- **Tools：** GSC 係基本盤，其他（SEMrush/Ahrefs/Screaming Frog）只用過一兩次
- **經驗：** 主要 on-page，但自認唔太識
- **Client CMS：** WordPress、Shopify、custom build
- **Client 類型：** 混合（corporate、e-commerce、brand site）
- **目標：** 一條龍——由頭到尾自己 handle

---

## Phase 1：GSC 實戰（零成本、即刻開始）

### 1.1 Performance 檢查

打開 GSC → Performance，重點睇 3 樣嘢：

| 指標 | 做咩 | 目標 |
|------|------|------|
| **Impressions vs Clicks** | 計 CTR | CTR < 2% 嘅 page 要優化 title / meta description |
| **Average position 11-20** | 呢啲最有潛力推上第一頁 | 優化呢啲 page 優先 |
| **對比 3 個月排名** | 搵 "lost rankings" | 排名跌咗嘅 page 要分析原因 |

### 1.2 URL Inspection

用 URL Inspection tool 檢查重要 page：

- [ ] Indexed？
- [ ] Canonical 正確？
- [ ] Mobile friendly？
- [ ] 如果有 "Discovered - currently not indexed" → 要處理（提交 index request / 加 internal link / 改善 content quality）

### 1.3 Sitemap + Coverage

- [ ] 確認 sitemap.xml 已提交
- [ ] Pages → 檢查有冇 error / excluded with warnings
- [ ] 修復 404s、soft 404s、redirect chains

---

## Phase 2：On-Page 優化（最核心嘅執行力）

### 2.1 Keyword Research（免費工具就夠）

**第一步：GSC 現有 keywords**
- GSC → Performance → 睇你而家 rank 緊嘅 keywords
- 搵出 position 11-20 嘅 keywords → 呢啲係「低掛果實」

**第二步：擴展 keywords**
- Google Autocomplete → 輸入 primary keyword，睇建議
- People Also Ask → 搵 long-tail 機會
- 每個 page 鎖定：1 個 primary keyword + 2-3 個 secondary

### 2.2 On-Page Checklist（逐頁做）

每個 page 逐項檢查：

- [ ] **Title tag** — 含 primary keyword，≤ 60 字元，有吸引點擊嘅 hook
- [ ] **Meta description** — 含 keyword，≤ 150 字元，有 CTA
- [ ] **H1** — 全頁只有一個，包含 primary keyword
- [ ] **H2-H3** — 包含 secondary keywords，結構化內容
- [ ] **URL** — 短、含 keyword、用 hyphen（`/seo-guide` 唔係 `/seo_guide`）
- [ ] **Internal links** — 每頁至少 3 個 internal link 指向相關頁面
- [ ] **Images** — 有 alt text（描述性 + keyword），壓縮大小（WebP 格式）
- [ ] **Content length** — 搜尋排名前 10 嘅 page 寫幾多字，最少要 match

### 2.3 Content 優化（AIO 層面）

- [ ] 加 **FAQ section** → 針對 People Also Ask 嘅問題
- [ ] 加 **Schema markup**（見 Phase 3.2）
- [ ] **E-E-A-T signals**：作者名、資歷、引用來源、日期

---

## Phase 3：Technical SEO

### 3.1 Audit Tools

**Google PageSpeed Insights（免費）**
- 檢查 Core Web Vitals：
  - LCP（Largest Contentful Paint）< 2.5s
  - CLS（Cumulative Layout Shift）< 0.1
  - INP（Interaction to Next Paint）< 200ms

**Screaming Frog（免費版 500 URLs）**
爬 client 嘅 site，搵：

| 問題 | 點搵 |
|------|------|
| Broken links (404s) | Response Code = 404 |
| Missing title / meta description | Page Title / Meta Description = 空 |
| Duplicate H1 | H1 Count > 1 |
| Redirect chains | Redirect Chains 報告 |
| Orphan pages | 喺 sitemap 但冇 internal link 指向 |

### 3.2 Schema Markup（Easy Win）

按頁面類型加 Schema：

| Schema 類型 | 用邊度 | 工具 |
|-------------|--------|------|
| **Organization** | 首頁 | Merkle Schema Generator |
| **Article / BlogPosting** | Blog post | Google Schema Markup Helper |
| **FAQPage** | 有 FAQ 嘅頁面 | Merkle Schema Generator |
| **Product** | E-commerce page（Shopify 通常自動有） | 檢查已存在 |
| **LocalBusiness** | 有實體店嘅 client | Merkle Schema Generator |

驗證工具：**Google Rich Results Test**

### 3.3 Robots.txt + Canonical

- [ ] 確認 robots.txt 冇 block 重要 page
- [ ] 每頁有正確 canonical tag
- [ ] WordPress：Yoast / RankMath 處理
- [ ] Shopify：通常自動處理

---

## Phase 4：持續執行系統

### Monthly Routine

1. **GSC Performance review** → 搵升跌嘅 keywords
2. **揀 3-5 個最有潛力嘅 page** → 做 on-page 優化
3. **檢查 new 404s / indexing issues** → 即刻修復
4. **更新 1-2 篇舊 content** → 加新資訊、更新 data、refresh 發佈日期

### Quarterly Deep Dive

1. **Screaming Frog full audit**
2. **Core Web Vitals 趨勢檢查**
3. **Competitor rankings 變化分析**
4. **Schema markup 全面檢查**

---

## 建議執行時間表

| 時間 | 任務 | 預計時間 |
|------|------|----------|
| **今日** | 打開任一 client 嘅 GSC，跟 Phase 1 走一次 | 30 分鐘 |
| **本週** | 搵 3 個 page，跟 Phase 2 checklist 逐項優化 | 2-3 小時 |
| **下週** | 裝 Screaming Frog，跑一次 audit（Phase 3.1） | 1-2 小時 |
| **第三週** | 試加 Schema markup 到 1-2 個 page（Phase 3.2） | 1 小時 |

---

## CMS 快速參考

### WordPress
- **SEO Plugin：** Yoast SEO 或 Rank Math（二揀一就夠）
- **Schema：** Plugin 自動處理大部分，手動加用 plugin 嘅 advanced section
- **Speed：** 用 WP Rocket 或 LiteSpeed Cache 做 caching，圖片用 WebP

### Shopify
- **SEO：** Theme 內建大部分 on-page 設定（title、meta description、alt text）
- **Schema：** Product / Organization 通常自動生成
- **Speed：** 選輕量 theme，壓縮圖片，減少 app 安裝數量

### Custom Build
- **需要手動處理所有嘢** — title、meta、canonical、schema、sitemap、robots.txt
- **建議：** 建立一個 SEO checklist template 畫俾 dev team follow

---

*最後更新：2026-05-23*
*來源：Ruga tailor-made SEO 實戰路線*
