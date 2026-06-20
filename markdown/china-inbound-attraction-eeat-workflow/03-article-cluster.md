# Step 3：文章集群拆分

### 目标

当一个景点主题过大时，拆成多篇互补文章。每篇文章只承担一个核心任务，避免内容重复和关键词内耗。

### 输入

```yaml
attraction: "Forbidden City"
serp_intents:
  - "practical guide"
  - "tickets"
  - "walking route"
  - "history and culture"
  - "nearby attractions"
  - "private guide"
business_goal:
  - "SEO traffic"
  - "trust building"
  - "inquiry conversion"
```

### 输出

```yaml
cluster_name: "Forbidden City Travel Guide Cluster"
pillar_article:
  title: "How to Visit the Forbidden City: A Practical Guide for First-Time Visitors"
  core_keyword: "how to visit Forbidden City"
  role: "总入口，解决第一次参观的完整规划"
supporting_articles:
  - title: "Forbidden City Tickets: Booking, Passport Rules, and Entry Tips"
    core_keyword: "Forbidden City tickets"
    role: "解决购票和入场焦虑"
  - title: "Best Forbidden City Walking Route: What to See in 2-4 Hours"
    core_keyword: "Forbidden City walking route"
    role: "解决路线和时间安排"
  - title: "Forbidden City History Explained for Travelers"
    core_keyword: "Forbidden City history for travelers"
    role: "解决文化理解和深度体验"
  - title: "Forbidden City, Tiananmen Square, and Jingshan Park One-Day Route"
    core_keyword: "Forbidden City one day itinerary"
    role: "解决北京一日路线组合"
  - title: "Do You Need a Guide for the Forbidden City?"
    core_keyword: "Forbidden City private guide"
    role: "承接导游和定制游转化"
cannibalization_risk:
  - "主文章和路线文章都可能争夺 how to visit，需要用标题、H1 和内容边界区分"
```

### 判断标准

拆分原则：

- 主文章解决“如何参观”。
- 配套文章解决更细问题。
- 产品文章解决“是否找导游/定制游”。
- 文化文章解决“为什么值得看、怎么看懂”。
- 路线文章解决“怎么安排一天或半天”。

不能出现：

- 两篇文章抢同一个主关键词。
- 每篇都写完整百科。
- 主文章和配套文章内容重复超过 30%。
- 内链没有上下游关系。
- 配套文章无法回到主文章或业务页面。

### 可复制 Prompt

```text
你是一名 Google SEO Topic Cluster 策略师，专注中国入境旅游网站。

请把下面这个景点主题拆成一个清晰的文章集群。

景点：{{attraction}}
SERP 意图：{{serp_intents}}
目标读者：
- 第一次来中国的海外游客
- 深度文化体验游客
- 海外旅行社/渠道伙伴

商业目标：
- SEO 流量
- 品牌权威
- 咨询/预订

请输出：

1. 是否需要文章集群
2. 主文章设计
3. 配套文章设计
4. 内链结构
5. 关键词内耗风险
```

---
