---
name: nrs-research
description: |
  Naval Ravikant / 纳瓦尔 research workflow with default IMA knowledge-base retrieval. Use when the user asks for a source-grounded synthesis, theme analysis, comparison, memo, or explanation about Naval's ideas on wealth, leverage, specific knowledge, judgment, happiness, reading, startups, angel investing, AI, decision-making, or life philosophy. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

# nrs-research

Produce source-grounded research notes from the Naval knowledge base.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use IMA retrieval before making source-specific claims. Read `references/query-map.md` for bilingual search expansion.

## Workflow

1. Restate the research question and define the scope.
2. Search IMA with 3-6 bilingual query terms.
3. Cluster results by theme, source type, and confidence.
4. Separate directly supported findings from inference.
5. Produce a compact memo with practical implications.

## Output Template

```markdown
# 研究备忘录

## 问题

## IMA 检索摘要
- 知识库：
- 检索词：
- 命中的材料：
- 证据强度：
- 缺口：

## 核心结论
1.
2.
3.

## 主题拆解

## 可迁移原则

## 适用边界

## 下一步
```

## Quality Bar

- Do not flatten Naval into generic self-help advice.
- Preserve tension between wealth, freedom, happiness, judgment, and long-term games.
- Do not invent direct quotes. Mark paraphrases as paraphrases.
- If evidence is thin, recommend follow-up IMA searches instead of overstating confidence.
