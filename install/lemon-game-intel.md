# 安装：游戏资讯日报 · 游戏情报员 角色技能（lemon-game-intel）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**游戏情报员**的完整作业技能：按主编派工单用 opencli 采集 Reddit / X 及指定网站的游戏资讯，经识图筛选后产出资讯包交主编审核。

## 安装步骤

依次执行以下命令（覆盖式安装，升级时重新执行同样的命令即可）：

```bash
git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p ~/.claude/skills
rm -rf ~/.claude/skills/lemon-game-intel
cp -r /tmp/lemon-agent-team/skills/lemon-game-intel ~/.claude/skills/
rm -rf /tmp/lemon-agent-team
```

## 备选方式（环境装有 skills CLI 时）

```bash
npx skills add azure1489/lemon-agent-team -s lemon-game-intel -g -y
```

## 安装后自检

执行：

```bash
ls ~/.claude/skills/lemon-game-intel ~/.claude/skills/lemon-game-intel/references
```

确认以下文件全部存在：

- `~/.claude/skills/lemon-game-intel/SKILL.md`
- `~/.claude/skills/lemon-game-intel/references/编辑部通讯录.md`
- `~/.claude/skills/lemon-game-intel/references/游戏资讯日报_交付与流转规范.md`

确认无误后，**重启会话**使技能生效。之后你以游戏情报员身份工作时，按 SKILL.md 中的流程开展工作即可。
