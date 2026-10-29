---
name: nrs-ima
description: |
  IMA retrieval bridge for Naval Ravikant / 纳瓦尔 workflows. Use when the user explicitly invokes $nrs-ima or asks to search, read, cite, summarize, verify, or troubleshoot Naval materials from IMA. This skill defaults to the IMA knowledge base named "纳瓦尔知识库 | 复利思维".
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# nrs-ima

Use this skill as the source-retrieval entry for Naval materials.

## Default Source

Default IMA knowledge base:

```text
纳瓦尔知识库 | 复利思维
```

Use the exact full name `纳瓦尔知识库 | 复利思维` unless the user explicitly names another IMA knowledge base.

Do not search for knowledge bases with the short keyword `纳瓦尔`. Do not list, compare, merge, or retrieve from other knowledge bases that merely contain `纳瓦尔` in the name. If the IMA tool returns multiple matches, choose only the exact match `纳瓦尔知识库 | 复利思维`.

## Required Dependency

- `ima-skill/SKILL.md`
- `ima-skill/knowledge-base/SKILL.md`

Do not invent IMA APIs. Do not expose internal `knowledge_base_id`, `media_id`, or `folder_id`.

If IMA credentials are missing, explain setup and stop:

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

## Query Guidance

Read `references/query-map.md` when choosing search terms.

Prefer bilingual query expansion:

- English concept: `specific knowledge`, `leverage`, `accountability`, `judgment`, `happiness`, `reading`, `wealth without luck`.
- Chinese concept: `特定知识`, `杠杆`, `责任`, `判断力`, `幸福`, `阅读`, `如何不靠运气致富`.

## Output Template

```markdown
## IMA 检索摘要
- 知识库：
- 检索词：
- 命中的材料：
- 可用证据：
- 不确定/缺失：

## 处理结果

## 下一步
```

## Rules

- Do not claim to have read IMA content unless retrieval actually happened.
- Use short source snippets only when needed; otherwise summarize.
- Separate source-backed findings from inference.
- If retrieval returns weak evidence, say so and propose better search terms.
