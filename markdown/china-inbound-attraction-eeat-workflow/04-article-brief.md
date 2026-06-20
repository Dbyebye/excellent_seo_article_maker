# Step 4：单篇文章 Brief

### 目标

把某一篇文章落实成可直接写作的内容简报，避免写作时跑题、泛化或漏掉 E-E-A-T 证据。

### 输入

```yaml
article_title: "How to Visit the Forbidden City"
article_role: "Pillar Article"
primary_keyword: "how to visit Forbidden City"
reader_problem: "第一次来北京，不知道如何顺利参观故宫"
target_audience:
  - "first-time visitors"
  - "culture travelers"
conversion_goal: "引导咨询北京私家导览或中国定制行程"
```

### 输出

```yaml
brief_status: "ready_to_write"
article_angle: "面向第一次来中国游客的实用参观指南，结合路线、票务、护照、文化背景和导游建议"
seo:
  primary_keyword: "how to visit Forbidden City"
  secondary_keywords:
    - "Forbidden City tickets"
    - "Forbidden City opening hours"
    - "Forbidden City route"
    - "Forbidden City guide"
  search_intent: "实用游览规划"
  meta_title: "How to Visit the Forbidden City: First-Timer Guide"
  meta_description: "Plan your Forbidden City visit with ticket, passport, route, timing, guide, and nearby attraction tips for first-time travelers."
outline:
  - "H1: How to Visit the Forbidden City"
  - "Quick Answer"
  - "Why Visit the Forbidden City"
  - "Tickets, Passport, and Entry Rules"
  - "Entrance, Exit, and Walking Route"
  - "What to See Inside"
  - "How Long to Spend"
  - "Best Time to Visit"
  - "Guide vs Self-Guided"
  - "Nearby Attractions"
  - "FAQ"
eeat_requirements:
  - "引用官方票务和开放时间来源"
  - "加入实地路线经验"
  - "标注信息更新时间"
  - "加入海外游客证件、支付、入口提醒"
conversion:
  soft_cta: "如果你希望把故宫和北京其他景点顺路安排，可以让本地顾问帮你设计路线。"
  hard_cta: "咨询北京私家导览/定制行程"
```

### 判断标准

一份合格 Brief 必须包含：

- SEO：核心关键词、辅助关键词、搜索意图、Meta title、Meta description、URL slug。
- 读者：用户是谁、当前焦虑、读完后能做什么决定。
- 内容：文章角度、H1、H2/H3 大纲、每节回答的问题。
- E-E-A-T：经验、专业、权威、可信证据。
- 转化：软 CTA、硬 CTA、内链、产品页链接位置。
- 更新：易过期信息和更新频率。

### 可复制 Prompt

```text
你是一名专业的 Google E-E-A-T 旅游文章 Brief 作者，专注中国入境旅游。

请为下面这篇文章生成完整写作 Brief。

文章标题：{{article_title}}
文章角色：{{article_role}}
核心关键词：{{primary_keyword}}
目标读者：{{target_audience}}
读者问题：{{reader_problem}}
商业目标：{{conversion_goal}}

请输出：

1. SEO 基础
2. 读者画像
3. 文章角度
4. 详细大纲
5. E-E-A-T 证据设计
6. 转化设计
7. 更新维护
```

---
