# Report Builder Evaluation — V1 Winnie Chiu SEO/AIO Diagnostic

**Evaluated:** 2026-06-16
**Evaluated by:** Ruga 🐻‍❄️
**Source Report:** `winniechiu-report-v1.md`

---

## Core Problem

**整份 report 缺乏 research methodology 透明度。** 唔知用咩 tool、幾時做嘅、query 係咩、結果點嚟 — 導致多個 factual errors。

---

## Section-by-Section Evaluation

### 1) 3 個最重要發現 — ❌ TOTAL FAIL

**Problems identified:**
- **"AIO 可見度極低"** — Bjai 親手喺 Copilot / Perplexity / Google AI Overview search 過 "best hk psychologist" 見到 Winnie 被引用。Report 結論與事實不符。
- **"Content 只有 3 頁"** — sitemap_index.xml 通常列晒所有 indexed URLs。Report 未貼出實際 crawl 結果，疑似 guesswork。
- **"缺少 Google Business Profile"** — Winnie 已有 GBP + reviews on Google Maps。Report 寫「致命缺失」係 factual error。
- E-E-A-T 信號不足嘅 claim 唔準確 — 有 GBP + reviews = 已有 E-E-A-T 基礎。

**Root cause 推測：**
1. AIO search 結果因地域、時間、個人化而唔同，report 可能冇控制變量
2. 可能根本冇做 live search，憑推測寫
3. Content 頁面數可能只 check 咗 post-sitemap 而非完整 sitemap_index

**Required fix:**
- 每個 claim 必須附 evidence（link / screenshot / data snippet）
- AIO 搜尋要記錄：日期、時間、地域、browser profile（logged-in / incognito）、exact query
- Content 頁面數要實際 crawl sitemap，列出具體 URLs

---

### 2) 測試 Keywords — ⚠️ DIRECTION OK, EXECUTION QUESTIONABLE

**Good:**
- Related keywords + search suggestions 嘅 gesture 正確

**Problems:**
- 結果準確度成疑 — Bjai 之前 search 有見到 Winnie，但 report 全部 ❌
- 「AIO 結論」語氣太武斷、太負面、極度唔 sales-driven
- 從「完全唔存在」寫法，應改為「已有基礎可見度，但 coverage 同競爭力可大幅提升」

**Required fix:**
- Search 要用多個 profile（incognito / VPN / mobile）同時做
- 中英文 query 都要 test（"psychologist Hong Kong" + "心理醫生 香港"）
- 語氣從 diagnostic 轉為 consultative

---

### 3) SEO 基礎健康 — ⚠️ OPACITY ISSUE

**Problems:**
- 寫咗一堆數字（HTTPS 100、Title 85 等），但冇講明：
  - 用咩 tool audit 嘅？（Lighthouse? Screaming Frog? 手動 check?）
  - 數字嘅 scoring criteria 係咩？
  - 網站速度 65 分嘅數據來源？
- 沒有可追溯性 = 客戶無法 verify

**Required fix:**
- 每項 audit 註明 tool / method
- 數字要有可追溯 source

---

### 4) AI 友善度 — ⚠️ MIXED

**正確部分：**
- Schema 分析（有但不足）大致準確
- Blog / Resource 缺失嘅判斷正確
- 多語言缺失嘅判斷正確

**錯誤部分：**
- Google Business Profile 條 — Winnie 已有 GBP，唔係「致命缺失」
- 應改為「已有 GBP 但可優化」（reviews 數量、post frequency、Q&A 等）

---

### 5) 競爭對手 AIO 對比 — ❌ SAME METHODOLOGY ISSUE

**Problems:**
- 如果 Winnie 嘅分析都錯，competitor 嘅分析一樣值得質疑
- 需要同一套 transparent methodology 才有比較價值
- 冇列出 competitor 嘅 search evidence

---

### 6) 機會缺口 — ⚠️ FORMAT OK, PRIORITY QUESTIONABLE

**OK:**
- Look and feel 可以接受
- Quick Win / 中期 / 長期 分層合理

**Problem:**
- Base data 錯 → recommended priority 可能錯
- 例如 GBP 唔係 quick win（因為已有），應該改為 GBP optimization

---

### 7) 華佗處方 Recommendations — ⚠️ NEEDS FACT-CHECK

**Problems:**
- Recommendation 應該先 fact-check 再寫
- 例如建議「建立 GBP」但 Winnie 已經有 — 會令客戶覺得 report 唔專業
- 需要 independent AI agent 做驗證

---

## Overall Assessment

| 維度 | 評分 | 評語 |
|---|---|---|
| 準確度 | 2/10 | 多個 factual errors，核心結論與事實不符 |
| 透明度 | 1/10 | 完全冇 methodology 說明，無法 verify |
| 語氣 | 3/10 | 太負面、太武斷、唔 sales-driven |
| 格式 | 7/10 | 結構清晰、visual OK |
| Actionability | 4/10 | 有 good gestures 但因 base data 錯而打折 |

**Overall: 3.4 / 10 — Report format 可用，但 content 需要完全重建**

---

## V2 Report Builder Requirements

### Must-Have
1. **Live Data Collection** — 每個 claim 基於實際 search/crawl，附 evidence
2. **Methodology Transparency** — 記錄 tool、query、timestamp、profile
3. **Independent Fact-Check Step** — 獨立 verify 每個結論
4. **Consultative Tone** — 正向但誠實，sales-driven
5. **Chinese + English Query Coverage** — 香港市場必須中英雙語

### Nice-to-Have
6. Screenshot / archive link 作為 evidence
7. Score 背後嘅 rubric 公開
8. Comparison baseline（定期 rerun 可比較）

---

_This evaluation will inform the V2 report builder workflow._
