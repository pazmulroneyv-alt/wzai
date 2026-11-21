# WZAI

WZAI 桌面客户端（插件版 / 无插件版），当前正式版本 v1.0（1.0.0）。

- 安装包：见 [Releases](https://github.com/pazmulroneyv-alt/wzai/releases)
- 内置更新器从本仓库的最新 Release 检查、下载并校验安装包
- 校验值：每个安装包附 `.sha256` 文件
- 局域网副本：`\\192.168.88.8\wz\wzagent开发\<系统>\wzai-v1.0`（插件版）与 `wzai-v1.0-noplugin`（无插件版）

## 支持的安装包

| 系统 | 插件版 | 无插件版 |
| --- | --- | --- |
| Windows x64 | `WZAI-1.0.0-win-x64.exe` | `WZAI-1.0.0-noplugin-win-x64.exe` |
| Linux x64 | `WZAI-1.0.0-linux-amd64.deb` | `WZAI-1.0.0-noplugin-linux-amd64.deb` |
| macOS Intel | `WZAI-1.0.0-mac-x64.dmg` | `WZAI-1.0.0-noplugin-mac-x64.dmg` |

Linux 为用户级安装：deb 仅放置只读安装源，程序安装到 `~/.wzai/app`，运行不需要 root。
