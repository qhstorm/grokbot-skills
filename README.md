# grokbot-skills

Jerry（qhstorm）在 Grok Bot 上用的自定义技能库。

这些技能对你名下所有 Grok Bot 全局共享（写进 `/home/box/agent-data/workflows/`）。

## 同步机制

- 本仓库对应云端电脑上的 `/home/box/agent-data/workflows/`
- 云端大约每 5 分钟执行一次 `git pull --rebase`，有本地改动时再 `git push`
- 本地 push 后最多约 5 分钟生效；云端改动会自动推回
- 使用技能时会重新读文件，一般不用重载；新建或改名的技能，标题和描述要等 Bot 处理过对话后才会出现在技能列表里

## 用法

1. 本地 clone 本仓库（或直接在本目录改）
2. 每个技能一个子目录，内含 `SKILL.md`（YAML frontmatter + 步骤）
3. commit + push，等同步即可

## 目录约定

```
workflows/
  <skill-id>/
    SKILL.md
  README.md
  AGENTS.md
```
