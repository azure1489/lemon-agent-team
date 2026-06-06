# lemon-agent-team · 游戏资讯日报编辑部

微信公众号「**每日花生新闻**」的多 Agent 编辑部：六个角色 Agent（飞书机器人）按「游戏资讯日报」六阶段流水线协作——情报采集 → 选题 → 视觉 ∥ 内容（并行） → 成品合成 → 发布，主编为中枢、唯一对接用户，每阶段经「主编审 + 用户审」两道闸。

## 角色技能安装

每个角色一个 skill。**把对应安装文档的链接发给该 Agent（hermes 飞书通道），Agent 读取文档后即可自助安装**：

| 角色 | Skill | 安装文档链接（直接发给 Agent） |
|---|---|---|
| 主编 | `lemon-chief-editor` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-chief-editor.md |
| 游戏情报员 | `lemon-game-intel` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-game-intel.md |
| 选题研究员 | `lemon-topic-researcher` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-topic-researcher.md |
| 视觉设计师 | `lemon-cover-designer` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-cover-designer.md |
| 深度内容作者 | `lemon-content-writer` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-content-writer.md |
| 发布员 | `lemon-publisher` | https://github.com/azure1489/lemon-agent-team/blob/main/install/lemon-publisher.md |

安装文档主方式为 `skills` CLI（`npx skills add azure1489/lemon-agent-team -s <skill名> -g -y`，自动探测 agent 环境并装到对应技能目录，不依赖特定路径）；环境无 Node/npx 时文档内附手动复制方式。升级 = 重发同一个链接（覆盖式安装）。

各 Agent 环境的前置依赖：`lark-cli`（编辑部群消息）、`aliyun-oss-delivery` skill（交付物上传 OSS）；另外游戏情报员需 `opencli` 与 vision toolset，视觉设计师需 `generate-images` skill，发布员需 `md2wechat` 与 `mp-helper` skill。

## 仓库结构

| 路径 | 说明 |
|---|---|
| `游戏资讯日报_交付与流转规范.md` | 总规范：交付形态、命名、OSS 路径、溯源 header、审核流转 |
| `游戏资讯日报_验收标准.md` | 主编审核用的逐条验收细则 |
| `作业手册_*.md` | 六份角色作业手册（skill 的内容源头） |
| `编辑部通讯录.md` | 飞书群「编辑部」各 Agent 的 Open ID |
| `html-guide.md` | 微信公众号 HTML 规范（发布员用） |
| `templates/` | 公众号文章样式模板（发布员用） |
| `skills/` | 六个可安装的角色 skill（由作业手册转写，自包含） |
| `install/` | 六份发给 Agent 的自助安装文档 |

> 维护注意：作业手册 / 规范改动后，须同步 `skills/` 下对应 SKILL.md 及各 skill 内的 references 副本，并 push 到 GitHub 后通知各 Agent 重新安装。详见 `CLAUDE.md`。
