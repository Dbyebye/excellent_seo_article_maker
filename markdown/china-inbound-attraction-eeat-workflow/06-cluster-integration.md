# Step 6：集群融合与内链审核

### 目标

把多篇文章融合成一个清晰的 Google 内容集群，避免文章孤岛、内容重复和关键词内耗。

### 输入

```yaml
cluster_articles:
  - title: "How to Visit the Forbidden City"
    role: "pillar"
  - title: "Forbidden City Tickets Guide"
    role: "support"
  - title: "Forbidden City Walking Route"
    role: "support"
  - title: "Do You Need a Guide for the Forbidden City?"
    role: "conversion"
business_pages:
  - "Beijing private tour"
  - "China cultural tour"
  - "Custom China itinerary"
```

### 输出

```yaml
cluster_status: "ready"
pillar_page: "How to Visit the Forbidden City"
supporting_pages:
  - "Forbidden City Tickets Guide"
  - "Forbidden City Walking Route"
  - "Forbidden City History Explained"
conversion_pages:
  - "Do You Need a Guide for the Forbidden City?"
internal_link_map:
  - from: "pillar"
    to: "tickets"
    anchor: "how to book Forbidden City tickets"
  - from: "pillar"
    to: "walking route"
    anchor: "best Forbidden City walking route"
  - from: "walking route"
    to: "private tour"
    anchor: "private Forbidden City guide"
content_gaps:
  - "缺少适合家庭游客的路线"
  - "缺少老人或行动不便游客建议"
  - "缺少雨天或旺季游览方案"
```

### 判断标准

集群完整性：

- 是否有明确主文章。
- 每篇文章是否有唯一任务。
- 是否有清晰上下游关系。
- 是否覆盖游客完整决策路径。
- 是否有连接到业务页面的转化路径。

内链要求：

- 主文章链接到所有配套文章。
- 配套文章回链主文章。
- 转化文章链接产品页或咨询页。
- FAQ 文章链接到具体解决方案。
- 内链锚文本要自然，不堆关键词。

关键词内耗检查：

- 标题是否过于相似。
- H1 是否抢同一关键词。
- 内容是否重复。
- 目标搜索意图是否混乱。

### 可复制 Prompt

```text
你是一名 Google SEO 内容架构师，专注旅游网站 Topic Cluster 和内链策略。

请审核下面这个景点文章集群是否已经形成完整内容体系。

文章列表：
{{cluster_articles}}

业务页面：
{{business_pages}}

请输出：

1. 集群结构判断
2. 每篇文章角色审核
3. 内链地图
4. 关键词内耗风险
5. 内容缺口
6. 最终集群输出
```

---
