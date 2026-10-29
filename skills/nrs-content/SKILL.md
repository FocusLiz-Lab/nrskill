---
name: nrs-content
description: |
  Naval Ravikant / 纳瓦尔 content workflow with default IMA knowledge-base retrieval. Use when the user wants content ideas, essay outlines, newsletters, scripts, social posts, threads, titles, hooks, or a content calendar based on Naval's ideas about wealth, leverage, judgment, happiness, learning, startups, investing, or life design. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


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
