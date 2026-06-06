# 安装：游戏资讯日报 · 主编 角色技能（lemon-chief-editor）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**主编**的完整作业技能：审核各阶段交付物、退回返工、转交用户审、写派工单派工、汇合成品、确认发布收尾。

## 安装步骤

依次执行以下命令（覆盖式安装，升级时重新执行同样的命令即可）：

```bash
git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p ~/.claude/skills
rm -rf ~/.claude/skills/lemon-chief-editor
cp -r /tmp/lemon-agent-team/skills/lemon-chief-editor ~/.claude/skills/
rm -rf /tmp/lemon-agent-team
```

## 备选方式（环境装有 skills CLI 时）

```bash
npx skills add azure1489/lemon-agent-team -s lemon-chief-editor -g -y
```

## 安装后自检

执行：

```bash
ls ~/.claude/skills/lemon-chief-editor ~/.claude/skills/lemon-chief-editor/references
```

确认以下文件全部存在：

- `~/.claude/skills/lemon-chief-editor/SKILL.md`
- `~/.claude/skills/lemon-chief-editor/references/编辑部通讯录.md`
- `~/.claude/skills/lemon-chief-editor/references/游戏资讯日报_交付与流转规范.md`
- `~/.claude/skills/lemon-chief-editor/references/游戏资讯日报_验收标准.md`

确认无误后，**重启会话**使技能生效。之后你以主编身份工作时，按 SKILL.md 中的流程开展工作即可。
