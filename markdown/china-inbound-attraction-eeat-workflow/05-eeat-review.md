# Step 5：E-E-A-T 内容审核

### 目标

审核文章是否真正 helpful、reliable、people-first，并体现 Experience、Expertise、Authoritativeness、Trustworthiness，而不是泛泛的 AI 景点介绍。

### 输入

```yaml
draft_article: "文章正文"
brief: "文章 Brief"
official_sources:
  - "景区官网"
  - "官方票务页面"
  - "政府或博物馆信息"
  - "Google Search Central"
```

### 输出

```yaml
publish_status: "needs_revision"
eeat_score:
  experience: 8
  expertise: 7
  authority: 6
  trust: 8
critical_issues:
  - "缺少官方票务来源"
  - "没有说明入口和出口"
  - "没有标注更新时间"
revision_actions:
  - "加入官方票务链接"
  - "补充推荐游览路线"
  - "增加适合家庭、老人、文化游客的差异建议"
```

### 判断标准

Experience 经验：

- 是否有真实游览路线。
- 是否提到入口、出口、排队、步行时间、拥挤点。
- 是否有第一次来中国游客的具体提醒。
- 是否有游客会踩坑的细节。

Expertise 专业：

- 是否解释为什么这么安排。
- 是否区分不同游客类型。
- 是否说明自助游和导游的差异。
- 是否把文化背景讲得准确且易懂。

Authoritativeness 权威：

- 是否引用官方来源。
- 是否使用景区、博物馆、政府、票务平台信息。
- 是否避免无来源断言。

Trustworthiness 可信：

- 是否标注更新时间。
- 是否提醒开放时间、票价、预约规则可能变化。
- 是否避免夸大承诺。
- 是否对安全、证件、支付、预约等事项讲清楚。

### 可复制 Prompt

```text
你是一名严格的 Google E-E-A-T 内容审核编辑，专注中国入境旅游行业。

请审核下面这篇文章是否满足 helpful、reliable、people-first 和 E-E-A-T 标准。

文章 Brief：
{{brief}}

文章正文：
{{draft_article}}

请按以下结构输出：

1. 总体判断
2. E-E-A-T 评分
3. Helpful Content 检查
4. 具体问题清单
5. 必须补充的信息
6. 修改优先级
```

---
