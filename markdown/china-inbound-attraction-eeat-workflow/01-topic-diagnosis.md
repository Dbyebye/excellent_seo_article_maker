# Step 1：主题诊断

### 目标

判断用户给出的景点主题适合写成单篇文章，还是应该拆成多篇文章集群。

### 输入

```yaml
topic: "故宫"
industry: "中国入境旅游"
audience:
  - "第一次来中国的海外游客"
  - "深度文化体验游客"
  - "海外旅行社/渠道伙伴"
business_goal:
  - "Google SEO 流量"
  - "品牌权威"
  - "咨询/预订转化"
language: "中文输出"
market: "Google 海外搜索"
```

### 输出

```yaml
topic_type: "景点级主题"
recommended_content_model: "单景点实用游览指南 + 配套文章"
need_cluster: true
primary_article: "How to Visit the Forbidden City"
supporting_articles:
  - "Forbidden City Tickets Guide"
  - "Best Forbidden City Walking Route"
  - "Forbidden City History Explained for Travelers"
  - "Forbidden City One-Day Route with Tiananmen and Jingshan"
  - "Do You Need a Guide for the Forbidden City?"
reason:
  - "主题包含门票、入口、路线、开放时间、交通、文化背景和是否需要导游等多个搜索意图"
  - "单篇文章承载全部意图会过长"
  - "需要用配套文章承接长尾搜索和转化需求"
```

### 判断标准

需要拆成多篇文章的信号：

- 一个主题包含多个搜索意图。
- 用户既想了解“是什么”，又想知道“怎么玩”。
- 涉及门票、交通、开放时间、路线、导游、季节、避坑等多类问题。
- 单篇文章会过长，影响阅读和转化。
- SERP 上同时出现 guide、tickets、itinerary、things to do、how to visit、best time、nearby attractions 等不同页面类型。

可以写成单篇文章的信号：

- 搜索意图集中。
- 景点不复杂，游览方式单一。
- 用户问题可以在一篇文章里完整解决。
- 没有明显对比、路线、深度文化解释或产品转化需求。

### 可复制 Prompt

```text
你是一名专业的 Google SEO 内容策略师，专注中国入境旅游行业和 E-E-A-T 内容规划。

请诊断下面这个旅游主题是否适合写成单篇文章，还是应该拆成文章集群。

主题：{{topic}}
目标读者：
- 第一次来中国的海外游客
- 深度文化体验游客
- 海外旅行社/渠道伙伴

商业目标：
- 获取 Google SEO 流量
- 建立品牌权威
- 获取咨询/预订

输出语言：中文

请按以下结构输出：

1. 主题类型判断
   - 城市级 / 景点级 / 路线级 / 对比级 / 榜单级 / FAQ 级

2. 用户真实搜索意图
   - 信息型
   - 计划型
   - 交易型
   - 对比型
   - 深度体验型

3. 是否需要拆成多篇文章
   - 结论：需要 / 不需要
   - 理由

4. 推荐内容模型
   - 主文章
   - 配套文章
   - 每篇文章的核心任务

5. 风险提醒
   - 是否容易写成百科
   - 是否容易关键词内耗
   - 是否需要更新信息
```

---
