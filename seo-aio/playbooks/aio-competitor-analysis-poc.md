# AIO Competitor Analysis — POC Workflow

> **Purpose:** Systematic framework for conducting AI Search Optimization (AIO) competitor analysis for logistics/3PL clients. Designed for Perplexity + Gemini + Google NotebookLM as complementary tools.
>
> **Version:** 1.0 | **Created:** 2026-06-23
>
> **Sample Client:** Yusen Logistics (adapt the competitor list and queries per client)

---

## Framework Overview

```
┌─────────────────────────────────────────────────┐
│  Layer 1: Define Competitive Universe           │  ← Perplexity
├─────────────────────────────────────────────────┤
│  Layer 2: Deep Competitive Content Audit         │  ← Gemini + NotebookLM
│  Layer 2.5: Source Knowledge Base (Grounding)   │  ← NotebookLM
├─────────────────────────────────────────────────┤
│  Layer 3: Prompt Intent Analysis                │  ← Perplexity + Gemini
│  Layer 4: Citation & Recommendation Analysis    │  ← Perplexity
│  Layer 4.5: Synthesis & Validation              │  ← NotebookLM
├─────────────────────────────────────────────────┤
│  Layer 5: Actionable AIO Strategy               │  ← Gemini (final)
└─────────────────────────────────────────────────┘
```

### Tool Roles

| Tool | Strength | Weakness | Role |
|---|---|---|---|
| **Perplexity** | Live web search, citations, real-time data | No deep cross-reference | Discovery & Testing |
| **Gemini** | Long analysis, framework building, structured output | Hallucination risk on facts | Strategy & Audit |
| **NotebookLM** | Multi-source digest, cross-reference, grounding | No live search, bounded by uploads | Validation & Synthesis |

---

## Layer 1: Define the Competitive Universe

**Tool:** Perplexity | **Purpose:** Find Yusen's real competitors in AI search — not ranking lists, but who AI actually cites when users ask logistics questions.

### Prompt 1 — AI Search Visibility Mapping

```
I'm conducting an AIO (AI Search Optimization) competitor analysis for [CLIENT NAME]. Please search across Google AI Overviews, ChatGPT, and your own index for the following query clusters:

**Query Cluster A (Brand Discovery):**
- 'best freight forwarding companies [REGION]'
- 'top 3PL providers for [INDUSTRY]'
- 'reliable [MODE] freight forwarder [ORIGIN] to [DESTINATION]'

**Query Cluster B (Problem-Solution):**
- 'how to reduce logistics costs for [INDUSTRY]'
- '[SPECIALTY SERVICE] logistics solutions for [SECTOR]'
- 'customs brokerage services [LOCATION]'

**Query Cluster C (Comparison/Intent):**
- '[CLIENT NAME] vs [COMPETITOR A]'
- '[CLIENT NAME] vs [COMPETITOR B] vs [COMPETITOR C]'
- '[CLOSEST COMPETITOR] vs [CLIENT NAME] freight services'

For each query, tell me:
(1) Which companies are mentioned/cited?
(2) Is [CLIENT NAME] mentioned?
(3) What position does [CLIENT NAME] appear (first, mentioned but not prominent, or absent)?
(4) What sources are cited for each mention?

Format results in a comparison matrix.
```

**Customization notes:**
- Replace `[CLIENT NAME]`, `[REGION]`, `[INDUSTRY]` etc. per client
- Add 3-5 queries per cluster; adjust based on client's actual service lines
- For Yusen-specific: include "Japan to US", "automotive logistics", "Asia Pacific"

---

## Layer 2: Deep Competitive Content Audit

**Tool:** Gemini | **Purpose:** Deep structural analysis of competitor content vs. client content for AIO-readiness.

### Prompt 2 — Structured Content Comparison

```
I need you to conduct a structured AIO content audit comparing [CLIENT NAME] against its top 5 competitors in AI search visibility. The competitors to analyze are:

1. [COMPETITOR 1]
2. [COMPETITOR 2]
3. [COMPETITOR 3]
4. [COMPETITOR 4]
5. [COMPETITOR 5]

For each competitor, analyze these AIO-readiness dimensions:

**A. Entity Authority (does AI recognize them as authoritative?)**
- Wikipedia presence and depth
- Knowledge panel completeness
- Structured data (schema.org Organization, FAQPage, HowTo, Service)
- Industry report mentions (Gartner, McKinsey, sector-specific rankings)

**B. Content Architecture for LLM Consumption**
- Do they have dedicated 'services' pages with clear entity definitions?
- FAQ / knowledge base content depth
- Blog/thought leadership frequency and topic coverage
- Technical documentation quality (API, integration guides)

**C. AI-Friendly Formatting**
- Use of structured headings (H1-H3 hierarchy)
- Listicles and comparison content
- Data-rich pages with statistics, case studies
- Multi-language content (especially relevant languages per market)

**D. Digital Footprint & Signals**
- Backlink profile strength (estimated)
- Social proof (LinkedIn, industry awards)
- Press release frequency and AI-newsworthiness
- ESG / sustainability content depth

Score each dimension 1-10 and provide a radar chart description for each competitor. Then rank all 6 (including [CLIENT NAME]) by overall AIO-readiness.
```

---

## Layer 2.5: Source Knowledge Base (Grounding)

**Tool:** Google NotebookLM | **Purpose:** Build a validated knowledge base from real source material to ground all subsequent analysis.

### Setup

1. Create a new Notebook in NotebookLM
2. Upload source material (see [Source Template](#source-template) below)
3. Use the following queries for cross-referencing

### NotebookLM Cross-Reference Queries

```
Query 1: "Compare the service descriptions of [CLIENT NAME] and [COMPETITOR 1]. What entity signals does each one include that would help AI tools understand their expertise?"

Query 2: "Based on the uploaded sources, which competitor has the most comprehensive thought leadership content? What topics do they cover that [CLIENT NAME] doesn't?"

Query 3: "What certifications, awards, and industry rankings are mentioned for each company? Which proof points are missing for [CLIENT NAME]?"

Query 4: "Compare the sustainability/ESG messaging across all competitors. Which ones have content that AI would surface for 'green logistics' or 'sustainable supply chain' queries?"
```

**Output use:** Feed NotebookLM findings into Gemini Prompt 2 to ground the audit with real source data.

---

## Layer 3: Prompt Intent Analysis

**Tool:** Perplexity + Gemini | **Purpose:** Understand what target audience asks AI tools, and where the client has coverage gaps.

### Prompt 3 — User Intent Discovery (Perplexity)

```
Act as a [INDUSTRY] industry analyst. I need to understand what questions [TARGET BUYER PERSONA] ask AI tools when evaluating [SERVICE CATEGORY] providers.

Please research and categorize the most common user intents:

**Intent 1: Vendor Selection**
- What do users ask when comparing providers?
- What criteria do they mention? (cost, reliability, coverage, technology, etc.)

**Intent 2: Problem-Solving**
- What problems do users bring to AI?
- Which providers get recommended for which problems?

**Intent 3: Validation/Trust**
- What due diligence questions do users ask?
- What proof points (certifications, case studies, rankings) do AI tools surface?

**Intent 4: Trend/Technology**
- What emerging technology questions appear?
- Which providers are associated with innovation/technology leadership?

For each intent category, give me 5-8 example queries and note whether [CLIENT NAME] would likely appear in AI responses.
```

### Prompt 4 — Gap Analysis from Intent Data (Gemini)

```
Based on the following user intent categories and queries for [SERVICE CATEGORY] provider evaluation, analyze where [CLIENT NAME] has content gaps that prevent AI from recommending or citing them:

[PASTE Perplexity Prompt 3 results here]

For each gap identified, suggest:
1. The specific content piece needed (blog post, FAQ, case study, comparison page, etc.)
2. The target query it should rank/cite for
3. The entity signals it needs to include
4. Priority level (High/Medium/Low) based on estimated search volume and business impact

Output as a prioritized content roadmap table.
```

---

## Layer 4: Citation & Recommendation Analysis

**Tool:** Perplexity | **Purpose:** Directly test client visibility across AI platforms.

### Prompt 5 — Direct Citation Test

```
I'm testing AI search visibility for specific logistics companies. Please answer each question and be transparent about which sources you're drawing from:

1. 'Who are the top 10 [SERVICE TYPE] companies in [YEAR]?' — Is [CLIENT NAME] in your response? If yes, at what position? If no, who occupies the positions [CLIENT NAME] should target?

2. 'Which [SERVICE TYPE] company has the strongest presence in [REGION] for [INDUSTRY]?' — Do you mention [CLIENT NAME]? Who do you mention instead?

3. 'What are [CLIENT NAME]'s core services and strengths?' — How comprehensive is your answer? What sources do you cite?

4. 'Compare [CLIENT NAME] vs [COMPETITOR A] vs [COMPETITOR B]' — How do you frame the comparison? What advantages do you attribute to each?

5. 'Which [SERVICE TYPE] companies use AI for [PROCESS]?' — Is [CLIENT NAME] mentioned for its recent partnerships/innovations? Who else is mentioned?

After answering all 5, give me an overall assessment: What does [CLIENT NAME] need to improve for AI tools to recommend them more prominently?
```

**Pro tip:** Run this same set of questions in ChatGPT and Claude too. Compare citation patterns across platforms — each AI has different source preferences and citation behavior.

---

## Layer 4.5: Synthesis & Validation

**Tool:** NotebookLM | **Purpose:** Cross-validate findings from Perplexity and Gemini, identify contradictions, assess confidence.

### Setup

1. Upload all previous outputs to the same Notebook (or a new "Analysis" Notebook):
   - Perplexity P1 results (competitive universe)
   - Perplexity P3 results (user intents)
   - Perplexity P5 results (citation test)
   - Gemini P2 results (content audit)
   - Gemini P4 results (gap analysis)

### NotebookLM Synthesis Query

```
I've uploaded findings from Perplexity and Gemini analyzing [CLIENT NAME]'s AI search visibility. Please:

1. Identify any contradictions between the Perplexity findings and Gemini analysis
2. For each competitor's AIO-readiness score, assess confidence level based on available evidence
3. Flag any claims that lack sufficient source support
4. Synthesize the most confident findings into a single executive brief (max 500 words)
```

---

## Layer 5: Actionable AIO Strategy

**Tool:** Gemini | **Purpose:** Final client-ready AIO strategy proposal, cross-validated by NotebookLM synthesis.

### Prompt 6 — Final AIO Strategy Synthesis

```
You are an AIO (AI Search Optimization) strategist. I'm presenting a competitive analysis for [CLIENT NAME]. Here are the findings:

[PASTE results from Prompts 1-5 AND NotebookLM synthesis here]

Based on all the data above, create a comprehensive AIO strategy proposal with:

**1. Executive Summary** (3-4 bullet points on [CLIENT NAME]'s current AI search position)

**2. Competitive Positioning Matrix**
- Where [CLIENT NAME] wins vs competitors in AI visibility
- Where [CLIENT NAME] loses vs competitors
- Where nobody wins (white space opportunities)

**3. Priority Content Initiatives** (Top 10)
- Each with: title, format, target AI query, entity signals to include, estimated impact

**4. Technical AIO Optimizations**
- Schema markup priorities
- Structured data recommendations
- Site architecture changes for LLM crawlability

**5. Measurement Framework**
- How to track AIO progress monthly
- KPIs: citation frequency, recommendation rate, query coverage
- Tools for monitoring AI visibility

**6. Quick Wins (30 days)** vs **Medium-term (90 days)** vs **Long-term (6 months)**

Format this as a client-ready presentation outline that could become a slide deck.
```

---

## Suggested Workflow

```
Day 1:  Perplexity P1 → competitive universe
Day 2:  📥 Upload sources to NotebookLM → build knowledge base
Day 3:  NotebookLM cross-reference queries → grounded insights
        Gemini P2 (fed with NotebookLM insights) → deeper audit
Day 4:  Perplexity P3 + P5 → intent analysis + citation test
Day 5:  Gemini P4 → gap analysis
Day 5:  📥 Upload all outputs to NotebookLM → synthesis check
Day 6:  Gemini P6 (final strategy, cross-validated) → client deliverable
```

---

## Source Template (NotebookLM Upload Checklist)

### Client Sources (Yusen Logistics example)

| # | Source Type | URL / File | Format | Notes |
|---|---|---|---|---|
| 1 | Corporate website — Services overview | `yusen.com/services/` | PDF export | Capture all service pages |
| 2 | Corporate website — About / Company profile | `yusen.com/about/` | PDF export | Entity signals, history, scale |
| 3 | Corporate website — Industries served | `yusen.com/industries/` | PDF export | Industry-specific positioning |
| 4 | Blog / News / Press releases | `yusen.com/news/` | PDF export | Last 12 months |
| 5 | Annual Report / Sustainability Report | Investor relations page | PDF download | ESG content, certifications |
| 6 | Case studies | `yusen.com/case-studies/` | PDF export | Social proof content |
| 7 | Recent partnership announcements | cargo.one press release (May 2026) | PDF | AI/tech signals |
| 8 | LinkedIn company page | `linkedin.com/company/yusen-logistics` | PDF export | Awards, updates |

### Competitor Sources (repeat for each competitor)

| # | Source Type | URL / File | Format | Notes |
|---|---|---|---|---|
| 1 | Corporate website — Services overview | Competitor website | PDF export | Key service pages only |
| 2 | Corporate website — About / Company profile | Competitor website | PDF export | Entity authority signals |
| 3 | Thought leadership / Blog (top 10) | Competitor website | PDF export | Topic coverage breadth |
| 4 | Annual Report / IR materials | Competitor IR page | PDF download | Scale, financials, priorities |
| 5 | Case studies / Client stories | Competitor website | PDF export | Social proof |
| 6 | Awards / Certifications page | Competitor website | PDF export | Trust signals |
| 7 | ESG / Sustainability report | Competitor website | PDF download | Sustainability positioning |

### Industry Sources

| # | Source Type | Source | Format | Notes |
|---|---|---|---|---|
| 1 | Armstrong & Associates Top 25 Freight Forwarders | `3plogistics.com` | Web page / PDF | Industry ranking authority |
| 2 | Transport Topics Top 100 Logistics | `ttnews.com/logistics/rankings/` | Web page / PDF | Revenue rankings |
| 3 | Gartner / McKinsey logistics reports | Research aggregator | PDF | If available |
| 4 | Inbound Logistics Top 100 Tech Providers | `inboundlogistics.com` | Web page / PDF | Technology positioning |
| 5 | Relevant Wikipedia pages | Wikipedia | PDF export | Entity authority baseline |
| 6 | Industry association directories | FIATA, JIFFA etc. | Web page | Regional authority signals |

### NotebookLM Notebook Structure Recommendation

- **Notebook 1: "Sources"** — All raw source material uploads
- **Notebook 2: "Analysis"** — All Perplexity/Gemini outputs + synthesis
- This separation keeps cross-referencing clean and prevents source material from diluting analysis outputs

---

## Pro Tips

- **Perplexity:** Use Focus mode (Academic) for higher source quality on research prompts
- **Gemini:** Use `@Search` to let it browse live before analyzing; paste NotebookLM findings as context
- **NotebookLM:** Don't overload — 50-60 sources max per notebook for optimal cross-referencing
- **Multi-platform testing:** Run Prompt 5 citation test in ChatGPT and Claude too; each AI has different citation patterns
- **Recent signals matter:** Flag any recent partnerships, acquisitions, or press releases that create "AI-newsworthy" content opportunities
- **Iterative prompts:** If any AI output seems thin, refine with follow-up questions before moving to the next layer
