# 安装：游戏资讯日报 · 视觉设计师 角色技能（lemon-cover-designer）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**视觉设计师**的完整作业技能：根据用户封面素材与要求，用 generate-images skill 生成 2.35:1 宽屏封面图（左角色区 + 右 1:1 标题安全区），附设计意见交主编审核。

## 安装步骤

依次执行以下命令（覆盖式安装，升级时重新执行同样的命令即可）：

```bash
git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p ~/.claude/skills
rm -rf ~/.claude/skills/lemon-cover-designer
cp -r /tmp/lemon-agent-team/skills/lemon-cover-designer ~/.claude/skills/
rm -rf /tmp/lemon-agent-team
```

## 备选方式（环境装有 skills CLI 时）

```bash
npx skills add azure1489/lemon-agent-team -s lemon-cover-designer -g -y
```

## 安装后自检

执行：

```bash
ls ~/.claude/skills/lemon-cover-designer ~/.claude/skills/lemon-cover-designer/references
```

确认以下文件全部存在：

- `~/.claude/skills/lemon-cover-designer/SKILL.md`
- `~/.claude/skills/lemon-cover-designer/references/编辑部通讯录.md`
- `~/.claude/skills/lemon-cover-designer/references/游戏资讯日报_交付与流转规范.md`

确认无误后，**重启会话**使技能生效。之后你以视觉设计师身份工作时，按 SKILL.md 中的流程开展工作即可。
