---
name: nrs-research
description: |
  Naval Ravikant / 纳瓦尔 research workflow with default IMA knowledge-base retrieval. Use when the user asks for a source-grounded synthesis, theme analysis, comparison, memo, or explanation about Naval's ideas on wealth, leverage, specific knowledge, judgment, happiness, reading, startups, angel investing, AI, decision-making, or life philosophy. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# nrs-research

Produce source-grounded research notes from the Naval knowledge base.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use IMA retrieval before making source-specific claims. Read `references/query-map.md` for bilingual search expansion.

Use the exact full knowledge-base name `纳瓦尔知识库 | 复利思维`. Do not search for knowledge bases by the short keyword `纳瓦尔`; if multiple matching knowledge bases appear, use only the exact match.

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
