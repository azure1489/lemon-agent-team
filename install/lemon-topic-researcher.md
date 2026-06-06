# 安装：游戏资讯日报 · 选题研究员 角色技能（lemon-topic-researcher）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**选题研究员**的完整作业技能：综合游戏情报员的资讯包，产出文章主标题（≤64 字符）、封面标题（≤2 行/每行 ≤5 字）与摘要（≤120 字符），交主编审核。

## 安装步骤

依次执行以下命令（覆盖式安装，升级时重新执行同样的命令即可）：

```bash
git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p ~/.claude/skills
rm -rf ~/.claude/skills/lemon-topic-researcher
cp -r /tmp/lemon-agent-team/skills/lemon-topic-researcher ~/.claude/skills/
rm -rf /tmp/lemon-agent-team
```

## 备选方式（环境装有 skills CLI 时）

```bash
npx skills add azure1489/lemon-agent-team -s lemon-topic-researcher -g -y
```

## 安装后自检

执行：

```bash
ls ~/.claude/skills/lemon-topic-researcher ~/.claude/skills/lemon-topic-researcher/references
```

确认以下文件全部存在：

- `~/.claude/skills/lemon-topic-researcher/SKILL.md`
- `~/.claude/skills/lemon-topic-researcher/references/编辑部通讯录.md`
- `~/.claude/skills/lemon-topic-researcher/references/游戏资讯日报_交付与流转规范.md`

确认无误后，**重启会话**使技能生效。之后你以选题研究员身份工作时，按 SKILL.md 中的流程开展工作即可。
