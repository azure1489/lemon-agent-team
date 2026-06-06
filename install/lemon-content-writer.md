# 安装：游戏资讯日报 · 深度内容作者 角色技能（lemon-content-writer）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**深度内容作者**的完整作业技能：根据选题与情报逐条整理 md 格式文章及配图（新游戏含发售时间/平台/港区价格，末尾固定页脚），交主编审核。

## 方式一：skills CLI 安装（推荐 · 通用）

`skills` CLI 会自动探测你所在的 agent 环境（Claude Code / Codex / Copilot / Gemini 等）并把技能装到该环境对应的技能目录，无须关心路径：

```bash
npx skills add azure1489/lemon-agent-team -s lemon-content-writer -g -y
```

升级：重新执行同一条命令即可。

## 方式二：手动安装（环境无 Node/npx 时）

先确定你的**全局技能目录**：即你当前环境中已安装技能所在的目录（例如 Claude Code 为 `~/.claude/skills`，其他 agent 环境以实际为准——查看你现有技能的存放位置即可）。下面用 `$SKILLS_DIR` 指代：

```bash
SKILLS_DIR=<替换为你的全局技能目录>

git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p "$SKILLS_DIR"
rm -rf "$SKILLS_DIR/lemon-content-writer"
cp -r /tmp/lemon-agent-team/skills/lemon-content-writer "$SKILLS_DIR/"
rm -rf /tmp/lemon-agent-team
```

两种方式都是覆盖式安装，升级时重新执行同样的命令即可。

## 安装后自检

到实际安装位置（方式一由 skills CLI 输出显示，方式二为 `$SKILLS_DIR/lemon-content-writer/`）确认以下文件全部存在：

- `SKILL.md`
- `references/编辑部通讯录.md`
- `references/游戏资讯日报_交付与流转规范.md`

确认无误后，**重启会话**使技能生效。之后你以深度内容作者身份工作时，按 SKILL.md 中的流程开展工作即可。
