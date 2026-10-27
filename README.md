# Iwildeer's VS Code Settings

- [`.vscode/settings.json`](./.vscode/settings.json)
- [`.vscode/extensions.json`](./.vscode/extensions.json)
- [`.vscode/global.code-snippets`](./.vscode/global.code-snippets)
- [`.claude/settings.example.json`](./.claude/settings.example.json)

## Preview

**Dark Mode**

![img](https://i.imgur.com/NsXj5ek.png "darkMode")

**Light Mode**

![img](https://i.imgur.com/rRbmQl8.png "lightMode")

## Extensions

Recommended extensions are listed in [`.vscode/extensions.json`](./.vscode/extensions.json), and will be prompted when opening the workspace. You can also install them all at once with:

```bash
extensions=(
  antfu.iconify
  antfu.smart-clicks
  antfu.icons-carbon
  antfu.theme-vitesse
  file-icons.file-icons
  dbaeumer.vscode-eslint
  usernamehw.errorlens
  streetsidesoftware.code-spell-checker
  ms-ceintl.vscode-language-pack-zh-hans
  stylelint.vscode-stylelint
  mhutchie.git-graph
  eamodio.gitlens
  bierner.color-info
  naumovs.color-highlight
  kisstkondoros.vscode-gutter-preview
  mikestead.dotenv
  bradlc.vscode-tailwindcss
  chakrounanas.turbo-console-log
  techer.open-in-browser
  vue.volar
  anthropic.claude-code
  pnp.polacode
)

for ext in "${extensions[@]}"; do
  code --install-extension "$ext"
done
```

| Category            | Extensions                                                                                                                                                                                                                     |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **antfu's**, ofc :P | `antfu.iconify`<br>`antfu.smart-clicks`                                                                                                                                                                                        |
| **Themes & Icons**  | `antfu.icons-carbon`<br>`antfu.theme-vitesse`<br>`file-icons.file-icons`                                                                                                                                                       |
| **Life Savers!**    | `dbaeumer.vscode-eslint`<br>`usernamehw.errorlens`<br>`streetsidesoftware.code-spell-checker`                                                                                                                                  |
| **Language**        | `ms-ceintl.vscode-language-pack-zh-hans`<br>`stylelint.vscode-stylelint`                                                                                                                                                       |
| **Git**             | `mhutchie.git-graph`<br>`eamodio.gitlens`                                                                                                                                                                                      |
| **Common**          | `bierner.color-info`<br>`naumovs.color-highlight`<br>`kisstkondoros.vscode-gutter-preview`<br>`mikestead.dotenv`<br>`bradlc.vscode-tailwindcss`<br>`chakrounanas.turbo-console-log`<br>`techer.open-in-browser`<br>`vue.volar` |
| **AI**              | `anthropic.claude-code`                                                                                                                                                                                                        |
| **PhotoShot**       | `pnp.polacode`                                                                                                                                                                                                                 |

## Claude Code

[`.claude/settings.example.json`](./.claude/settings.example.json) 是 [Claude Code](https://claude.com/claude-code) 的配置文件模板（通过 GLM 的 Anthropic 兼容端点接入）。

使用方法：在仓库根目录下复制模板到 `~/.claude/settings.json`，并填入你自己的 API Key：

```sh
cp .claude/settings.example.json ~/.claude/settings.json
```

各配置项说明：

| 配置项                                           | 说明                                  |
|-----------------------------------------------|-------------------------------------|
| `ANTHROPIC_AUTH_TOKEN`                        | API Key，**切勿提交真实 Key 到仓库**          |
| `ANTHROPIC_BASE_URL`                          | API 中转地址，此处为智谱 GLM 的兼容端点            |
| `API_TIMEOUT_MS`                              | 请求超时时间（毫秒）                          |
| `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC`    | 关闭非必要网络流量                           |
| `CLAUDE_CODE_AUTO_COMPACT_WINDOW`             | 自动压缩上下文的窗口大小                        |
| `ANTHROPIC_DEFAULT_{HAIKU,SONNET,OPUS}_MODEL` | 将 Haiku / Sonnet / Opus 档位映射到实际模型   |
| `effortLevel`                                 | 默认推理力度：`low` / `medium` / `high`    |
| `modelSettings`                               | 各模型独立的推理力度                          |
| `model`                                       | 默认使用的档位：`haiku` / `sonnet` / `opus` |

> ⚠️ API Key 属于敏感信息，请只使用 `<your-api-key>` 之类的占位符，不要把真实 Key 提交到任何仓库。

## LICENSE

MIT
