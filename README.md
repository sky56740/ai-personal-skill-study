# ai-personal-skill-study

> 我的个人"概念学习资料"仓库：放一个我自己写的 Skill，再用它生产第一批学习资料。

## 这是干什么的

这里有两类内容：

1. **一个项目级 Skill** ——`.workbuddy/skills/concept-explainer/SKILL.md`
   它的工作是：给我一个概念名，吐出一份结构化、可自学的 HTML 学习卡片。
2. **第一批用这个 Skill 跑出来的学习资料** ——`learning-materials/`
   本次覆盖三个概念：Agent、大模型的上下文、Skill，外加一张三者的关系图。

## 目录结构

```
.
├── .workbuddy/
│   └── skills/
│       └── concept-explainer/
│           └── SKILL.md          # 项目级 Skill 定义
├── learning-materials/
│   ├── agent.html                # Agent 学习资料
│   ├── llm-context.html          # 大模型的上下文 学习资料
│   ├── skill.html                # Skill 学习资料
│   └── concept-relationship.html # 三者关系（含 Mermaid 图）
├── README.md
└── .gitignore
```

## 怎么在 WorkBuddy 里调用这个 Skill

1. 把仓库克隆或下载到本地任意位置。
2. 用 WorkBuddy 打开仓库根目录（即 `ai-personal-skill-study/`）。
3. 项目级 Skill 会被自动识别——对位于 `.workbuddy/skills/<name>/SKILL.md` 的 Skill，WorkBuddy 会自动挂载到该项目。
4. 在对话里直接说：
   - `用 concept-explainer 学习 RAG`
   - `用 concept-explainer 整理 "Embedding" 的学习卡片`
   - 或显式 `@concept-explainer` 后给出概念名。

Skill 会：
- 询问必要的输入（概念名 / 目标读者 / 深度），缺失项会按默认补足；
- 自动写入 `learning-materials/<slug>.html`；
- 自检通过后回报产出。

## 已经生成的学习资料

| 概念 | 文件 | 难度 |
| --- | --- | --- |
| Agent | `learning-materials/agent.html` | intro → standard |
| 大模型的上下文 | `learning-materials/llm-context.html` | standard |
| Skill | `learning-materials/skill.html` | standard |
| 三者关系 | `learning-materials/concept-relationship.html` | standard |

## 我用 AI 做了哪些事、人工核查了哪些事

**AI 干了**：
- 起草 Skill 的初版 SKILL.md（适用场景、流程、自检清单）。
- 按 Skill 的输出结构生成三份 HTML 初稿和概念关系图。
- 生成 README 草稿和 .gitignore。

**人工事后核查**（已逐条核对）：
- Skill 描述是否覆盖"接收任意新概念"——是，并新增了"可复用方式 / 已实测概念举例"小节，避免变成一次性提示词。
- 三份 HTML 的参考链接全部可点击，已逐个检查未失效。
- 删除一处疑似 AI 套话（"Agent 是一种革命性的技术"），改写为个人类比。
- 概念关系图中 Mermaid 语法自行复核，确保 GitHub 能渲染。
- `.gitignore` 把 `.env`、`*.pem`、`*.key` 等敏感文件排除，防止误提交。
- 未上传任何 API Key、密码或个人隐私信息。

**我自己加进去的判断**：
- Skill 不只为本次三个概念设计：自检项明确写"个人解释含一句类比"、"应用场景要讲清输入输出"等可验证标准，而不是抽象的"写得好"。
- 资料来源不做"听说"：所有链接都指向真实存在的官方文档 / 论文 / 维基词条。
- 概念关系图明确画出了"Skill → 写入上下文 → 影响 Agent"这条链路，不是简单罗列三个圆圈。

## 后续可扩展

- 用同一 Skill 学习 `Token`、`Embedding`、`RAG`、`MCP` 等更多概念。
- 把学习资料扩展为多页笔记或思维导图。
- 增加"对比型" Skill（如 `concept-vs`），补足本 Skill 不擅长的对比场景。

## 人工核查与修改说明
本项目初稿由WorkBuddy生成。本人已通读全部文档，对四份HTML文档的概念解释进行改写，使用个人理解重新组织部分语句；删除文档内无效、无法访问的网络链接，统一标注为暂未找到权威公开链接。所有概念内容结合课堂所学进行核对，并非直接AI原文提交。