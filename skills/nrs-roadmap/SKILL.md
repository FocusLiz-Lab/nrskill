---
name: nrs-roadmap
description: |
  Naval Ravikant / 纳瓦尔 roadmap workflow with default IMA knowledge-base retrieval. Use when the user wants to apply Naval's ideas to personal wealth-building, career choice, learning, happiness, reading, startup decisions, investing judgment, life design, or a 7/30/90-day action plan. Defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

# nrs-roadmap

Convert Naval ideas into a practical action plan for the user's situation.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use IMA retrieval for Naval-specific principles. If retrieval is unavailable, state that the plan is based on general reasoning and should be verified against IMA.

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
