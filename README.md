# dsh-job-dev

dev 数字员工岗位包（每岗位一个独立包，与 dsh-job-secretary 同构）。

## 内容（单目录平铺）

| 文件 | 安装去向 | 作用 |
|---|---|---|
| `agent.cordis.yml` | `$DSH_HOME/.agent-presets/dev/` | 岗位 preset 组合：岗位 persona + skill 加载 |
| `preset.yml` | `$DSH_HOME/.agent-presets/dev/` | preset 显示元数据 |
| `SKILL.md` | `$DSH_HOME/skills/dev/` | 岗位技能：岗位专项方法 |

> preset 与 skill 同名同位：preset 落 `$DSH_HOME/.agent-presets/dev/`，skill 落 `$DSH_HOME/skills/dev/`（SKILL.md frontmatter `name: dev`）。

## 安装

- 开发期：用 job-install 插件（本地源 → DSH_HOME），或拷本目录到 user preset root / skills root。
- 生产期：dsh-himarket 安装发布包。

## 发布

推 `v*` tag 触发 GitHub Actions 自动 `npm publish`（需仓库配置 `NPM_TOKEN`）。
