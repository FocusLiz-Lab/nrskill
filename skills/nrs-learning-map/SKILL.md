---
name: nrs-learning-map
description: |
  Naval Ravikant / 纳瓦尔 learning-map workflow with default IMA knowledge-base retrieval. Use when the user asks where to start, what to read first, how to study Naval's wealth, happiness, judgment, leverage, reading, startups, or philosophy materials, or how to turn the "纳瓦尔知识库 | 复利思维" IMA knowledge base into a study plan, reading sequence, lesson map, or output-driven learning path.
---

# nrs-learning-map

Turn the Naval knowledge base into a focused learning path tied to the user's goal.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use `ima-skill/SKILL.md` and `ima-skill/knowledge-base/SKILL.md` for retrieval. Search IMA before recommending specific materials. Do not expose internal IMA IDs.

Read `references/archive-map.md` if you need a high-level map of the local source categories.

## Intake

Ask only for missing information:

```text
1. 你学习纳瓦尔的目标是什么：财富、杠杆、判断力、幸福、阅读学习、创业投资，还是整体人生框架？
2. 你现在处于哪一阶段：没看过、看了一点、想做内容、想用于职业/创业/投资决策？
3. 你想要什么输出：学习路径、阅读顺序、实战任务、内容选题，还是个人行动计划？
```

## Suggested Paths

- Wealth path: wealth without luck -> specific knowledge -> leverage -> accountability -> judgment -> compounding.
- Happiness path: desire -> peace -> health -> relationships -> meditation/awareness -> daily practice.
- Judgment path: mental models -> reading -> decision quality -> long-term games -> choosing people.
- Startup/investing path: founder thinking -> product/market judgment -> angel investing -> technology leverage.
- Content path: core theses -> contradictions -> modern applications -> personal examples -> publishable angles.

## Output Template

```markdown
# 纳瓦尔学习地图

## 你的目标

## IMA 检索摘要
- 知识库：
- 检索词：
- 命中的材料：
- 可用证据：
- 不确定/缺失：

## 先看这 5 个
1.
2.
3.
4.
5.

## 7 天启动计划

## 30 天学习顺序

## 每次学习必须产出的东西

## 下一步 Skill
```

## Quality Bar

- Do not recommend "全部从头看".
- Every learning plan must produce an artifact: decision memo, belief audit, content outline, habit experiment, reading note, or next action.
- If IMA retrieval is unavailable, state the limitation clearly.
