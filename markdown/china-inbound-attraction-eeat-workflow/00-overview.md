# 中国入境旅游景点内容 E-E-A-T 工作流

版本：v0.2  
适用场景：中国入境旅游网站，面向 Google 海外搜索，以景点内容为主。  
默认输出语言：中文  
目标读者：第一次来中国游客、深度文化体验游客、海外旅行社/渠道伙伴。  
核心目标：Google SEO 流量、品牌权威、咨询/预订转化。

参考原则：

- Google Helpful Content: https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- Google SEO Starter Guide: https://developers.google.com/search/docs/fundamentals/seo-starter-guide

---

# 总：工作流总览

## 1. 总目标

把一个中国景点主题，系统拆解成适合 Google SEO 的内容方案。

整套工作流需要同时解决 6 件事：

1. 判断主题适合单篇文章还是文章集群。
2. 识别 Google 海外用户的真实搜索意图。
3. 拆分主文章、配套文章和转化文章。
4. 生成可直接写作的单篇文章 Brief。
5. 审核文章是否满足 E-E-A-T 和 Helpful Content 标准。
6. 建立清晰的内容集群、内链结构和咨询/预订转化路径。

## 2. 默认策略

```yaml
industry: "中国入境旅游"
content_unit: "景点为主，城市作为上层归属"
default_model: "单景点实用游览指南 + 必要配套文章"
output_language: "中文"
seo_market: "Google 海外搜索"
target_audience:
  - "第一次来中国游客"
  - "深度文化体验游客"
  - "海外旅行社/渠道伙伴"
business_goal:
  - "获取 Google SEO 流量"
  - "建立品牌权威"
  - "获取咨询/预订"
```

## 3. 总原则

- 不写纯百科式景点介绍，除非百科信息服务于游客决策。
- 优先解决海外游客的真实问题：怎么去、怎么买票、是否需要护照、怎么玩、玩多久、是否需要导游、如何避坑、附近怎么组合。
- 涉及门票、开放时间、签证、交通、支付、预约等高变化信息时，必须查证官方或权威来源，并标注更新时间。
- 当主题过大时，拆成多篇文章配合，而不是把所有搜索意图塞进一篇文章。
- 每篇文章必须有唯一核心任务，避免关键词内耗。
- 主文章负责总入口，配套文章负责细分问题，转化文章负责承接咨询或预订。

## 4. 总流程

```text
Step 1. 主题诊断
  ↓
Step 2. SERP 与用户意图分析
  ↓
Step 3. 文章集群拆分
  ↓
Step 4. 单篇文章 Brief
  ↓
Step 5. E-E-A-T 内容审核
  ↓
Step 6. 集群融合与内链审核
  ↓
最终融合 Prompt
  ↓
后续封装为 Codex Skill
```

## 5. 每个分模块的固定输出

每个流程模块都必须包含：

- 目标
- 输入
- 输出
- 判断标准
- 可复制 Prompt

## 6. 总输出模板

当用户给出一个中国景点主题时，最终应该输出：

```yaml
topic: "景点主题"
topic_type: "城市级 / 景点级 / 路线级 / 对比级 / 榜单级 / FAQ 级"
recommended_model: "单篇文章 / 文章集群"
pillar_article:
  title: "主文章标题"
  role: "总入口，解决核心搜索意图"
supporting_articles:
  - title: "配套文章标题"
    role: "解决一个细分问题"
conversion_articles:
  - title: "转化文章标题"
    role: "承接咨询、导游、定制游等商业目标"
eeat_requirements:
  - "官方来源"
  - "实地经验"
  - "更新时间"
  - "游客风险提示"
internal_links:
  - from: "主文章"
    to: "配套文章"
    anchor: "自然锚文本"
```
