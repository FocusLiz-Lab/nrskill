---
name: nrs-roadmap
description: |
  Naval Ravikant / 纳瓦尔 roadmap workflow with default IMA knowledge-base retrieval. Use when the user wants to apply Naval's ideas to personal wealth-building, career choice, learning, happiness, reading, startup decisions, investing judgment, life design, or a 7/30/90-day action plan. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# nrs-roadmap

Convert Naval ideas into a practical action plan for the user's situation.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use IMA retrieval for Naval-specific principles. If retrieval is unavailable, state that the plan is based on general reasoning and should be verified against IMA.

Use the exact full knowledge-base name `纳瓦尔知识库 | 复利思维`. Do not search for knowledge bases by the short keyword `纳瓦尔`; if multiple matching knowledge bases appear, use only the exact match.

## Intake

Ask only for missing information:

```text
1. 你要解决的具体问题是什么？
2. 当前约束是什么：时间、钱、技能、工作、家庭、健康、风险承受度？
3. 你希望计划覆盖 7 天、30 天、90 天，还是一年？
```

## Workflow

1. Diagnose the user's current bottleneck.
2. Retrieve 3-5 relevant Naval principles from IMA.
3. Translate principles into constraints, tradeoffs, and actions.
4. Define a plan with leading indicators and review cadence.
5. Add anti-patterns: what not to do because it violates the principle.

## Output Template

```markdown
# 纳瓦尔行动路线图

## 当前问题

## IMA 检索摘要

## 可用原则
1.
2.
3.

## 7 天行动

## 30 天行动

## 90 天方向

## 指标

## 不要做

## 复盘问题
```

## Quality Bar

- Keep the plan concrete and falsifiable.
- Do not turn philosophy into vague affirmations.
- Show tradeoffs: optionality vs focus, leverage vs skill, freedom vs responsibility, desire vs peace.
- Do not give financial, legal, or medical advice as professional guidance.
