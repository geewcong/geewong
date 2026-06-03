# Google Ads Search Ads Experiment Framework

> 解決「0→1 最難」嘅問題。唔需要你由空白開始諗——跟住填空就得。
> 適用於 ad copy testing + ad group targeting + audience segment rationale。

---

## 核心原則

**你嘅問題唔係唔識諗，而係面對空白唔知由邊度開始。** 所以呢個 framework 唔係教你「點樣諗 idea」，而係俾你一個 **已經有結構嘅起點**，你做嘅只係填空同選擇。

每次測試只改 **一個變數**。改兩樣就唔知邊樣有效。

---

## Phase 0：搞清楚 Baseline（30 分鐘）

**唔好諗新 idea 先。先搞清楚你而家站喺邊。**

### 0.1 拉 Search Term Report

去 Google Ads → 報表 → 搜尋字詞報表。Export 最近 30-90 日嘅數據。

### 0.2 揀你要優化嘅 campaign

問自己：
- [ ] 邊個 campaign 消耗最大？
- [ ] 邊個 campaign CTR 最低？（最值得測）
- [ ] 邊個 campaign CPA / ROAS 最差？（最有改善空間）

**揀一個。** 唔好一次搞幾個。

### 0.3 記低現有數據

| 指標 | 現有數值 |
|------|----------|
| Impressions | |
| CTR | |
| Avg CPC | |
| Conv. rate | |
| CPA / ROAS | |
| Top impression share | |
| Search lost IS (budget) | |
| Search lost IS (rank) | |

呢個就係你嘅 baseline。之後所有測試都同呢個比。

---

## Phase 1：搵測試 Idea（唔使由零諗）

### 1.1 Ad Copy 測試 Idea Generator

**唔使自己諗。喺下面揀。**

#### A. 痛點角度（Pain Point）

你嘅客戶嘅客有咩痛？填空：

```
我嘅 target audience 最怕 ___________
我嘅 product/service 解決嘅最大問題係 ___________
佢哋而家用開嘅方案有咩唔好？___________
```

然後將答案變成 ad copy：

| 痛點 | 測試 Copy 方向 | Example |
|------|---------------|---------|
| 太貴 | 價格相關 messaging | "Save 30% vs Competitors" |
| 太慢 | 速度相關 | "Same-Day Results Guaranteed" |
| 唔可靠 | 信任相關 | "Trusted by 10,000+ Businesses" |
| 複雜 | 簡化相關 | "Setup in 5 Minutes, No Tech Needed" |
| 怕做錯決定 | 風險消除 | "Free Trial — Cancel Anytime" |

#### B. 受眾動機角度（Motivation）

你嘅客戶嘅客想達到咩？

```
佢哋最想得到嘅結果係 ___________
佢哋 success 嘅樣貌係 ___________
佢哋用完我哋 service 之後生活會點唔同？___________
```

| 動機類型 | 測試 Copy 方向 | Example |
|----------|---------------|---------|
| 慳時間 | 效率 messaging | "Get It Done in Half the Time" |
| 賺更多錢 | ROI messaging | "Increase Revenue by 40%" |
| 升職/成長 | 成就 messaging | "The Tool Top Marketers Use" |
| 安心 | 保障 messaging | "24/7 Support, Zero Downtime" |
| 社交認同 | FOMO messaging | "Join 500+ Companies Who Switched" |

#### C. 競爭對手角度（Competitor）

```
我哋最大嘅競爭對手係 ___________
佢哋做唔到但我哋做到嘅係 ___________
佢哋嘅客有咩 complaint？___________
```

| 測試方向 | Example |
|----------|---------|
| 直接比較 | "Better Than [Competitor] — Here's Why" |
| 差異化 | "The Only Platform With [Unique Feature]" |
| 轉會誘因 | "Switch From [Competitor] — Get First Month Free" |

⚠️ 注意：Google Ads 對競爭對手商標有政策限制，唔好直接用 competitor brand name 做標題，放描述度或者用 landing page 表達。

---

### 1.2 Audience Segment 測試 Idea Generator

#### 點搵 segment rationale？用呢個填空：

```
我嘅 product/service 最適合 ___________（行業/角色/情境）
佢哋通常喺 ___________（時間/季節/事件）最需要我
佢哾搜尋嘅時候用嘅字眼反映佢哋喺 ___________ 階段（認知/考慮/決策）
```

#### 常見 Segment 切法（揀 1-2 個測）：

| Segment 類型 | 點 set | Rationale |
|-------------|--------|-----------|
| **購買意圖** | In-market audience | 佢哋而家主動搵緊，CTR 同 conv. rate 會高 |
| **再營銷** | Website visitor (7/30/90日) | 已經認識個 brand，warm lead，CPA 低 |
| **相似受眾** | Similar audience from converter list | 搵同現有客似嘅人，擴大 reach 但維持質素 |
| **人口統計** | Age / Gender / Income | 如果 product 有明確 demographics，可以分開測 messaging |
| **地域** | City / Region / Radius | 唔同地區可能有唔同痛點（例如港島 vs 九龍） |
| **時間** | Ad schedule (dayparting) | B2B 工作時間 vs B2C 晚上時段 |
| **裝置** | Device (Mobile / Desktop / Tablet) | Mobile 用家行為唔同，可能需要唔同 CTA |

#### Rationale 寫法模板：

> 我假設 **[segment]** 會對 **[messaging angle]** 有更高 CTR，因為 **[原因]**。
> 例如：我假設 **in-market audience（搜尋 "SEO service"）** 會對 **"Free SEO Audit"** 嘅 ad 有更高 CTR，因為 **佢哋已經喺考慮階段，直接俾具體價值比空泛 brand message 更有效**。

寫完呢句，你就有 rationale。唔使 PhD 級別嘅分析。

---

### 1.3 Ad Group 結構建議

#### 選項 A：按意圖分（推薦）

```
Ad Group 1: Brand（品牌相關 keyword）
Ad Group 2: Problem-aware（痛點 keyword，e.g. " 點樣提升SEO"）
Ad Group 3: Solution-seeking（方案 keyword，e.g. "SEO服務推薦"）
Ad Group 4: Competitor（競爭對手 keyword）
Ad Group 5: Long-tail（具體長尾 keyword）
```

#### 選項 B：按受眾分

```
Ad Group 1: Cold — In-market
Ad Group 2: Warm — Website visitor 30日
Ad Group 3: Hot — Cart abandon / converter 180日
```

**揀一個。唔好兩個溝埋。**

---

## Phase 2：設定 Experiment（20 分鐘）

### 2.1 Google Ads 內置 Experiment

用 **Draft & Experiment** 功能：
- 原有 campaign = Control
- 複製一個 Draft = Variant
- 喺 Variant 改你要測嘅嘢（只改一樣）
- 設定 traffic split（建議 50/50）
- 設定日期（最少 2-4 週，視乎流量）

### 2.2 要改咩？對照表

| 我想測試... | 改咩 | 唔好改 |
|-------------|------|--------|
| 邊個 headline 吸引 | Headline 1-3 | Description、Landing page |
| 邊個 CTA 有效 | Description 2 / CTA 部分 | Headline、Keyword |
| 邊個 pain point 打中 | 整個 ad copy angle | Landing page、Targeting |
| 邊個 segment 好 | Audience segment | Ad copy、Landing page |
| Landing page 轉唔轉 | Landing page URL | Ad copy、Targeting |

### 2.3 最低要求

- 每個 variant 至少 **1,000 impressions** 先有統計意義
- 如果流量低，延長測試期或者加 budget
- 唔好少過 2 週就收結論

---

## Phase 3：睇結果（測試期完之後）

### 3.1 邊個指標贏咗？

| 測試目標 | 睇咩指標 |
|----------|----------|
| CTR 提升 | CTR（廣告點擊率） |
| 轉換提升 | Conv. rate, CPA |
品牌認知 | Impression share, CTR |
| 成本優化 | CPC, CPA |

### 3.2 結果判斷

| 結果 | 做咩 |
|------|------|
| Variant 明顯贏 | Apply to original campaign，結束 experiment |
| 差唔多 | 延長測試 or 揀成本低嗰個 |
| Variant 輸咗 | 保留 original，記錄 learning，試下一個 idea |

### 3.3 記錄 Learning

每次測試完，記低：

```
日期：
Campaign：
測試咗咩（改動）：
Hypothesis：
結果（數據）：
贏/輸/平手：
Learning：
下一步：
```

呢個 log 就係你嘅 **測試資產**。做完幾次你會開始見到 pattern，之後諗 idea 會越嚟越快。

---

## 快速起步 Checklist（0→1 版）

遇到空白腦嘅時候，跟住做：

- [ ] 拉 Search Term Report（10 min）
- [ ] 揀一個最差/最大嘅 campaign（5 min）
- [ ] 填低 Baseline 數據（5 min）
- [ ] 由「痛點角度」揀一個方向（5 min）
- [ ] 寫 2-3 個 variant headline（10 min）
- [ ] 開 Draft & Experiment，50/50 split（10 min）
- [ ] 啟動

**由空白到啟動測試：45 分鐘。**

之後就係等數據。你最擅長嘅 1→100 就會自然發生——因為你有數據可以優化。

---

## 心態提醒

- **唔需要完美嘅 hypothesis。** 「我覺得 A 會好過 B 因為 [一個理由]」就夠。
- **測試失敗唔係浪費。** 知道咩唔 work 同知道咩 work 一樣有價值。
- **你嘅 0→1 問題，解法係「填空」唔係「創作」。** 唔好坐喺空白 screen 前諗，打開呢個文件，填空，就行。
- **每個月至少跑一個 experiment。** 累積嘅 learning 先係真正嘅資產。
