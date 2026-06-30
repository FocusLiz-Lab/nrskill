---
name: nrs
description: |
  Naval Ravikant / 纳瓦尔 skill toolbox main router with default IMA knowledge-base grounding. Use when the user asks about Naval Ravikant, 纳瓦尔, wealth without luck, specific knowledge, leverage, judgment, happiness, reading, learning, startup/angel investing philosophy, decision-making, life design, content ideas, research summaries, or how to study the Naval knowledge base. By default, use the IMA knowledge base named "纳瓦尔知识库 | 复利思维". Triggers include $nrs, /nrs, Naval, Naval Ravikant, 纳瓦尔, 如何不靠运气致富, 财富, 杠杆, 判断力, 幸福, 人生真相, 学习地图, 研究分析, and IMA检索.
---

# nrs

This is the SkillHub root entry. For the full toolbox, use the skills under `skills/`.

## Default IMA Knowledge Base

```text
纳瓦尔知识库 | 复利思维
```

Use this exact full knowledge-base name for retrieval. Do not search for knowledge bases with the short keyword `纳瓦尔`, and do not enumerate or merge other matching knowledge bases. If the tool returns multiple matches, select only the exact match `纳瓦尔知识库 | 复利思维` unless the user explicitly asks to use another knowledge base.

## Routes

| User intent | Route to |
|---|---|
| Learning path or reading order | `$nrs-learning-map` |
| Source search, citation, IMA troubleshooting | `$nrs-ima` |
| Research synthesis or theme comparison | `$nrs-research` |
| Content ideas, outlines, scripts, posts | `$nrs-content` |
| Personal roadmap or action plan | `$nrs-roadmap` |

## Required Dependency

Use `ima-skill` for retrieval. If it is missing, tell the user:

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

Do not expose internal IMA IDs. Do not copy long source passages. Do not invent quotes, dates, tweets, or episode titles.
