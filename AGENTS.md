# 给 Agent 的说明

- 用户技能只放在本仓库（`/home/box/agent-data/workflows/`）
- Cursor 托管技能与插件技能是只读的，不要往本仓库里拷
- 新建技能：子目录 slug（kebab-case）+ `SKILL.md`；frontmatter 需要 `name` 与 `description`（description 写清何时使用）
- 技能正文保持通用模板；账号、频道、仓库等个性化内容写在例程或对话里，不要写进技能
- 同步脚本由 Grok Bot 例程驱动；冲突时优先保留 remote，rebase 失败就 abort 并上报
