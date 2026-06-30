# nrskill

Naval Ravikant / 纳瓦尔风格学习、研究、内容创作和个人行动计划 Skill 工具箱。

本仓库打包了一组面向 Agent 的 workflow skills，用于基于 IMA 知识库学习纳瓦尔资料，并完成学习路径、主题研究、内容选题、资料检索和行动路线图。

适用于 Codex、Claude Code、Cursor、Trae Solo 等支持 skill / system prompt 工作流的 Agent。

---

## 安装

```bash
npx -y skills add FocusLiz-Lab/nrskill -g --all
```

GitHub 仓库：`FocusLiz-Lab/nrskill`

## IMA 配置

默认 IMA 知识库名称：

```text
纳瓦尔知识库 | 复利思维
```

所有 workflow 默认使用这个知识库。用户明确指定其他 IMA 知识库时，优先使用用户指定名称。

检索时应精确使用完整名称 `纳瓦尔知识库 | 复利思维`，不要用 `纳瓦尔` 做知识库模糊搜索；如果出现多个匹配，只选择完整名称一致的这个知识库。

如果未安装 IMA skill：

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

## 加入 / 访问知识库

![纳瓦尔知识库二维码](docs/knowledge-base-qrcode.png)

## 工具箱

| Skill | 用途 |
|---|---|
| `$nrs` | 主入口，识别用户意图并路由到合适 workflow。 |
| `$nrs-ima` | 检索、核对、引用、排错 IMA 资料。 |
| `$nrs-learning-map` | 生成纳瓦尔资料学习路径、阅读顺序和学习任务。 |
| `$nrs-research` | 做财富、杠杆、判断力、幸福、阅读、创业投资等主题研究。 |
| `$nrs-content` | 把纳瓦尔思想转成选题、标题、脚本、长文大纲或内容日历。 |
| `$nrs-roadmap` | 把纳瓦尔原则转成 7/30/90 天个人行动计划。 |

## 常见路径

- 想系统学习：`$nrs-learning-map`
- 想找原始资料或核对出处：`$nrs-ima`
- 想研究一个主题：`$nrs-research`
- 想做内容：`$nrs-content`
- 想应用到职业、财富、学习或生活：`$nrs-roadmap`

## 使用示例

```text
$nrs-learning-map 系统学习这个知识库，先看哪些？
$nrs-research 纳瓦尔说的 specific knowledge 和 leverage 到底是什么关系？
$nrs-content 围绕“如何不靠运气致富”生成 10 个公众号选题。
$nrs-roadmap 我想用纳瓦尔的方法规划未来 30 天学习和赚钱路径。
$nrs-ima 帮我检索纳瓦尔关于 happiness 和 desire 的资料。
```

## 资料边界

本仓库只发布 workflow、资料地图和抽象后的知识原子，不发布原始 PDF、推文全文、视频逐字稿、课程材料或未授权资料。具体引用、原文核对和出处确认必须回到 IMA 或用户提供的合法来源。

## 许可证

CC BY-NC 4.0。仅限非商业学习、研究和个人工作流使用。
