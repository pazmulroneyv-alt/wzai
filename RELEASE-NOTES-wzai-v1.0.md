## WZAI v1.0（1.0.0）正式发布

首个 1.0 正式版，提供插件版与无插件版，覆盖 Windows / Linux / macOS。

### 主要更新

- 媒体模型适配：muse-video / muse-image / MiniMax-H3 支持参考图、参考视频、参考音频；MiniMax-H3 参考图上限放开到 9 张
- 新增模型族：gpt-image-2.5 / gpt-image-2.6（含 `xhigh`、`max` 质量档）、MiniMax-H3-Image、seedance 2.0 / 2.5
- 模型能力目录更新至 2026-11-19.1，客户端按目录声明自动适配
- 内置 Release 更新器：Windows 安装包、Linux 用户级 deb、macOS 均支持检查 Release、下载并按 SHA-256 校验后安装
- Linux 采用用户级安装：系统仅放置只读安装源，程序位于 `~/.wzai/app`，无需 root 运行
- 媒体按钮一次性发送等交互修正

### 安装包

| 系统 | 插件版 | 无插件版 |
| --- | --- | --- |
| Windows x64 | `WZAI-1.0.0-win-x64.exe` | `WZAI-1.0.0-noplugin-win-x64.exe` |
| Linux x64 | `WZAI-1.0.0-linux-amd64.deb` | `WZAI-1.0.0-noplugin-linux-amd64.deb` |
| macOS Intel | `WZAI-1.0.0-mac-x64.dmg` | `WZAI-1.0.0-noplugin-mac-x64.dmg` |

### 校验值（SHA-256）

```
acaecb538ffec29c05e576a0c14b5af77c6f08f086c760c6f078b0b52ba00373  WZAI-1.0.0-win-x64.exe
2d408d19bbd8a1f29b987271641e5645187f7def87e7a7404e7ec63bf7beb343  WZAI-1.0.0-noplugin-win-x64.exe
56b1386fa7c71ad23f0db942688f3b26f280702e0bfd555266de5ec0447cd675  WZAI-1.0.0-linux-amd64.deb
59427e2c9a16dd06a5120cd3a3b28e90ee4f0729007cde4c1b4914a39fe9cf40  WZAI-1.0.0-noplugin-linux-amd64.deb
71878d82d2ba2e99eb34b0d82256025e921fd1bb62eb428f1cd27f21aeac4499  WZAI-1.0.0-mac-x64.dmg
634f32c96537d4a493b834da5ed509b951290cdf95957e30a3e4042a0386bfcd  WZAI-1.0.0-noplugin-mac-x64.dmg
```

每个安装包同时附有 `.sha256` 文件，供更新器校验使用。

### 说明

- Windows 安装包未做代码签名；macOS 未做公证。
- 已在本机与开发机完成干净安装验证，功能验收请人工启动确认。
