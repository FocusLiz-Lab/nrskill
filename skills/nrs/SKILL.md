---
name: nrs
description: |
  Naval Ravikant / 纳瓦尔财富与判断力 Skill 工具箱主入口。用于不靠运气致富、特定知识、杠杆、判断力、幸福、阅读、学习、创业/天使投资哲学、决策、人生设计、内容选题、研究总结和纳瓦尔知识库学习路径。默认使用 IMA 知识库「纳瓦尔知识库 | 复利思维」，并可在 IMA 不可用时读取本地原子库。触发词包括 $nrs、/nrs、Naval、Naval Ravikant、纳瓦尔、如何不靠运气致富、财富、杠杆、判断力、幸福、人生真相、学习地图、研究分析和 IMA检索。
---

# nrs 纳瓦尔财富与判断力工具箱

这是 Naval Ravikant / 纳瓦尔财富与判断力工具箱的主入口。先判断用户意图，再路由到最相关的 workflow；如果上下文足够，直接在同一回答中完成对应工作流。

## 默认 IMA 知识库

所有 workflow skills 默认读取：

```text
纳瓦尔知识库 | 复利思维
```

用户不需要每次输入这个知识库名称。如果用户明确指定其他 IMA 知识库，则优先使用用户指定的知识库。

检索时必须使用完整名称 `纳瓦尔知识库 | 复利思维`。不要只用 `纳瓦尔` 做知识库模糊搜索，也不要合并其他相似知识库。若 IMA 返回多个结果，除非用户明确指定其他知识库，否则只选择完整名称一致的这个知识库。

## 必要依赖

所有需要资料依据的 workflow 都使用 `ima-skill` 做检索：

- `ima-skill/SKILL.md`
- `ima-skill/knowledge-base/SKILL.md`

不要臆造 IMA API。不要向用户暴露内部 `knowledge_base_id`、`media_id` 或 `folder_id`。

如果没有安装 `ima-skill` 或凭证缺失，先提示用户安装并配置 IMA：

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

## 路由表

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
