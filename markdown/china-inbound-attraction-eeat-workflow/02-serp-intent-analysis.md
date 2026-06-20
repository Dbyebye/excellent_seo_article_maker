# Step 2：SERP 与用户意图分析

### 目标

确认 Google 用户搜索这个景点时真正想解决什么问题，而不是按我们自己的理解写景点介绍。

### 输入

```yaml
attraction: "Forbidden City"
primary_keyword: "how to visit Forbidden City"
secondary_keywords:
  - "Forbidden City tickets"
  - "Forbidden City opening hours"
  - "Forbidden City walking route"
  - "Forbidden City guide"
target_market:
  - "US"
  - "UK"
  - "Australia"
  - "Europe"
```

### 输出

```yaml
serp_page_types:
  - "travel guide"
  - "ticket guide"
  - "itinerary"
  - "tour product page"
  - "official site"
dominant_intent: "实用游览规划"
secondary_intents:
  - "怎么买票"
  - "是否需要护照"
  - "从哪里进入"
  - "怎么玩不绕路"
  - "需要多久"
  - "是否需要导游"
  - "附近景点如何组合"
content_gap:
  - "竞品缺少海外游客视角"
  - "竞品缺少实地路线"
  - "竞品缺少文化解释"
  - "竞品缺少可信更新时间"
recommended_angle: "面向第一次来中国游客的实用参观指南，结合路线、票务、文化背景和避坑提醒"
```

### 判断标准

SERP 调研优先查看：

- Google SERP 前 10 名页面。
- People Also Ask。
- Reddit、Tripadvisor、旅行论坛。
- YouTube 标题和评论区问题。
- 竞品旅游公司文章。
- 景区官网或官方票务信息。
- Google Search Central 官方规范。

判断用户意图时重点看：

- 用户是在找“介绍”，还是找“参观方法”。
- 用户是否关心门票、护照、预约、入口、交通、路线。
- 用户是否在比较自助游和导游。
- 用户是否需要把该景点放进一日或多日行程。
- 用户是否需要文化解释来理解景点价值。

### 可复制 Prompt

```text
你是一名 Google SERP 分析师，专注中国入境旅游内容。

请围绕以下景点主题做 SERP 和用户意图分析：

景点：{{attraction}}
核心关键词：{{primary_keyword}}
辅助关键词：{{secondary_keywords}}
目标市场：{{target_market}}

请基于 Google 搜索结果、People Also Ask、旅游论坛、Tripadvisor、Reddit、YouTube、竞品旅游网站和官方信息，输出：

1. SERP 页面类型
2. 用户真实意图
3. 高频问题清单
4. 竞品内容缺口
5. 本站文章机会
6. 输出推荐
```

---
