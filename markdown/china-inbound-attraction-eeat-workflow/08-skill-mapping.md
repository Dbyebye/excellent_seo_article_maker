# 后续转 Skill 的模块映射

## 主 Skill 建议

未来可封装为一个主 skill：

```yaml
skill_name: "china-inbound-travel-content"
description: "中国入境旅游 Google E-E-A-T 内容工作流。用于景点主题诊断、SERP 意图分析、文章集群拆分、单篇文章 Brief、E-E-A-T 审核和内链融合。"
```

## 内部模块映射

```yaml
modules:
  topic_diagnosis:
    source_step: "Step 1"
    purpose: "判断主题颗粒度和是否需要文章集群"
  serp_intent_analysis:
    source_step: "Step 2"
    purpose: "分析 Google SERP 和海外游客真实需求"
  cluster_planning:
    source_step: "Step 3"
    purpose: "拆分主文章和配套文章，定义每篇文章核心任务"
  article_brief:
    source_step: "Step 4"
    purpose: "生成可写作的单篇文章 Brief"
  eeat_review:
    source_step: "Step 5"
    purpose: "审核文章是否满足 E-E-A-T 和 Helpful Content 要求"
  cluster_integration:
    source_step: "Step 6"
    purpose: "审核文章集群、内链、转化路径和关键词内耗"
```

## Skill 封装原则

- 一个主 skill，内部按模块组织，不拆成多个独立 skills。
- `SKILL.md` 只保留核心工作流和路由说明。
- 详细 prompt 可放入 `references/prompts.md`。
- 示例输入输出可放入 `references/examples.md`。
- 暂不写脚本，除非后续需要自动生成 Brief、检查 Markdown 结构或批量处理关键词。

## 后续验收标准

封装成 skill 前，至少用 3 个景点试跑：

- 故宫 Forbidden City
- 兵马俑 Terracotta Warriors
- 长城 Mutianyu / Badaling / Jinshanling

每个景点都要验证：

- 是否能正确判断单篇 vs 集群。
- 是否能输出不互相抢关键词的文章列表。
- 是否能给出实用、可信、面向海外游客的 Brief。
- 是否能指出 E-E-A-T 缺口。
- 是否能形成主文章、配套文章、产品页之间的内链路径。
