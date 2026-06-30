---
name: nrs
description: |
  Naval Ravikant / 纳瓦尔 skill toolbox main router with default IMA knowledge-base grounding. Use when the user asks about Naval Ravikant, 纳瓦尔, wealth without luck, specific knowledge, leverage, judgment, happiness, reading, learning, startup/angel investing philosophy, decision-making, life design, content ideas, research summaries, or how to study the Naval knowledge base. By default, use the IMA knowledge base named "纳瓦尔知识库 | 复利思维". Triggers include $nrs, /nrs, Naval, Naval Ravikant, 纳瓦尔, 如何不靠运气致富, 财富, 杠杆, 判断力, 幸福, 人生真相, 学习地图, 研究分析, and IMA检索.
---

# nrs

Act as the main router for the Naval Ravikant skill toolbox. Identify the user's intent and route to the most relevant workflow. If enough context exists, execute the routed workflow in the same answer.

## Default IMA Knowledge Base

All workflow skills default to:

```text
纳瓦尔知识库 | 复利思维
```

Users do not need to mention this knowledge-base name. If they explicitly name another IMA knowledge base, use that name instead.

## Required Dependency

All source-grounded workflows use `ima-skill` for retrieval:

- `ima-skill/SKILL.md`
- `ima-skill/knowledge-base/SKILL.md`

Do not invent IMA APIs. Do not expose internal `knowledge_base_id`, `media_id`, or `folder_id` to the user.

If `ima-skill` is not installed or credentials are missing, tell the user to install/configure IMA first:

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

## Route Map

| User intent | Route to | Use when |
|---|---|---|
| Learning path, reading order, where to start | `$nrs-learning-map` | User asks how to study Naval, which materials to read first, or how to navigate the knowledge base. |
| Source search, citation, IMA troubleshooting | `$nrs-ima` | User explicitly asks to search/read/cite IMA, list evidence, or debug retrieval. |
| Research synthesis, theme comparison, source-backed summary | `$nrs-research` | User wants to analyze wealth, leverage, judgment, happiness, startups, investing, AI, reading, or recurring ideas across sources. |
| Content ideas, posts, scripts, essays, threads | `$nrs-content` | User wants to turn Naval ideas into content angles, outlines, scripts, newsletters, or social posts. |
| Personal roadmap, 7/30/90-day actions, decision plan | `$nrs-roadmap` | User wants to apply Naval ideas to work, wealth-building, learning, happiness, career, or life design. |

## Clarify Once

If the user is vague, ask one question:

```text
你现在最想处理哪一块：学习路径、IMA资料检索、主题研究、内容创作，还是把纳瓦尔的方法用于个人行动计划？
```

After the answer, route immediately.

## Handoff Format

```text
这个问题交给 $skill-name。
原因：{one sentence}
需要输入：{what the user should provide next, if anything}
```

## Quality Bar

- Default to IMA-grounded workflows for substantive claims about Naval.
- Do not imitate Naval's persona.
- Do not invent quotes, episode titles, dates, tweets, or book claims.
- Do not copy long passages from books, PDFs, podcasts, tweets, or transcripts.
- Distinguish Naval's own ideas from later interpretation or user-provided context.
- Prefer concrete outputs: route, study sequence, research memo, content map, action plan, or next-week tasks.
