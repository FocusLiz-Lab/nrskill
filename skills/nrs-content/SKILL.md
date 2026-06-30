---
name: nrs-content
description: |
  Naval Ravikant / 纳瓦尔 content workflow with default IMA knowledge-base retrieval. Use when the user wants content ideas, essay outlines, newsletters, scripts, social posts, threads, titles, hooks, or a content calendar based on Naval's ideas about wealth, leverage, judgment, happiness, learning, startups, investing, or life design. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

# nrs-content

Turn Naval ideas into publishable content while keeping source boundaries clear.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use IMA retrieval for source-grounded topics. Do not copy long passages from tweets, books, transcripts, or PDFs.

Use the exact full knowledge-base name `纳瓦尔知识库 | 复利思维`. Do not search for knowledge bases by the short keyword `纳瓦尔`; if multiple matching knowledge bases appear, use only the exact match.

## Intake

Ask only for missing information:

```text
1. 内容平台是什么：公众号、X/Twitter、小红书、视频、播客、Newsletter，还是长文？
2. 目标读者是谁？
3. 你要选题、标题、脚本、长文大纲、成稿，还是内容日历？
```

## Workflow

1. Search IMA for the target theme.
2. Extract 3-7 abstract principles, not raw text.
3. Match principles to the audience's pain, aspiration, or decision.
4. Generate angles with tension: counterintuitive claim, tradeoff, mistake, practice, or story.
5. Include source-boundary notes when claims depend on IMA.

## Output Templates

For topic generation:

```markdown
# 纳瓦尔内容选题

## IMA 检索摘要

## 10 个选题
| 标题 | 核心观点 | 适合平台 | 证据/边界 |
|---|---|---|---|

## 推荐先做的 3 个
```

For a draft:

```markdown
# 标题

## 开头

## 主体

## 结尾

## 来源边界
```

## Quality Bar

- Do not write as Naval or imply endorsement.
- Prefer clear modern applications over quote collections.
- Keep output original and transformative.
- Avoid invented anecdotes, dates, or source claims.
