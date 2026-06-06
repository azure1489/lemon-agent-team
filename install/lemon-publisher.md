# 安装：游戏资讯日报 · 发布员 角色技能（lemon-publisher）

> 本文档供 Agent 自助安装。按下面步骤执行后，你将获得「游戏资讯日报」（微信公众号「每日花生新闻」）**发布员**的完整作业技能：把成品 md 用 md2wechat 转 HTML（套样式模板）、插入广告组件、用 mp-helper 把图片上传素材库并替换链接、上传微信公众号草稿箱（作者 CCS_Lemon），然后先通知主编。

## 安装步骤

依次执行以下命令（覆盖式安装，升级时重新执行同样的命令即可）：

```bash
git clone --depth 1 https://github.com/azure1489/lemon-agent-team /tmp/lemon-agent-team
mkdir -p ~/.claude/skills
rm -rf ~/.claude/skills/lemon-publisher
cp -r /tmp/lemon-agent-team/skills/lemon-publisher ~/.claude/skills/
rm -rf /tmp/lemon-agent-team
```

## 备选方式（环境装有 skills CLI 时）

```bash
npx skills add azure1489/lemon-agent-team -s lemon-publisher -g -y
```

## 安装后自检

执行：

```bash
ls ~/.claude/skills/lemon-publisher ~/.claude/skills/lemon-publisher/references ~/.claude/skills/lemon-publisher/assets/templates
```

确认以下文件全部存在：

- `~/.claude/skills/lemon-publisher/SKILL.md`
- `~/.claude/skills/lemon-publisher/references/编辑部通讯录.md`
- `~/.claude/skills/lemon-publisher/references/游戏资讯日报_交付与流转规范.md`
- `~/.claude/skills/lemon-publisher/references/html-guide.md`
- `~/.claude/skills/lemon-publisher/assets/templates/每日花生新闻_样式模版.html`
- `~/.claude/skills/lemon-publisher/assets/templates/每日花生新闻_索尼发布会_样式模版.html`

确认无误后，**重启会话**使技能生效。之后你以发布员身份工作时，按 SKILL.md 中的流程开展工作即可。
