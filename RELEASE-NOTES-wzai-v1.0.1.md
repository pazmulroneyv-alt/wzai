## WZAI v1.0.1 正式发布

WZAI 1.0.1 维护更新，统一发布插件版与无插件版，覆盖 Windows / Linux / macOS（x64）。

### 主要更新

- **聊天媒体工具与第三方供应方媒体模型共存**：
  - 接入 `.wzconfig` 渠道配置后，聊天输入框媒体工具不再因切换至第三方文本模型供应方而隐藏，仍可正常使用内置 WZAI 媒体能力；
  - 图像 / 视频 / 音频媒体选择器支持以分组形式同时展示 WZAI 模型与已导入或自定义的第三方供应方媒体模型；
  - 新增后端双向 `tool_choice` 路由（`wzai_media_routing`），确保选择 WZAI 模型时强制路由至 `wzai_generate`，选择第三方供应方模型时自动分流至桌面通用媒体工具并准确剥离前缀标识。
- **双版本更新器容错增强**：
  - `GithubReleaseStrategy` 新增 `/releases?per_page=10` 兜底检索与 `-(no)?plugin` 版本号后缀兼容；
  - 插件版与无插件版继续统一归档在同一个 GitHub Release（`wzai-v1.0.1`）下，防止两个版本互相串包并确保 1.0.0 用户均可平滑检查并升级。

### 安装包

| 系统 | 插件版 | 无插件版 |
| --- | --- | --- |
| Windows x64 | `WZAI-1.0.1-win-x64.exe` | `WZAI-1.0.1-noplugin-win-x64.exe` |
| Linux x64 | `WZAI-1.0.1-linux-amd64.deb` | `WZAI-1.0.1-noplugin-linux-amd64.deb` |
| macOS Intel | `WZAI-1.0.1-mac-x64.dmg` | `WZAI-1.0.1-noplugin-mac-x64.dmg` |

### 校验值（SHA-256）

```
3fd4904cc7f4a811565fa9af6fea313899e99369fa554435c3ef27df62dd05ae  WZAI-1.0.1-win-x64.exe
580d20e9e36513eef77d5fa807a03158f007a6c316bf703dd33d83f9d9bb9a9c  WZAI-1.0.1-noplugin-win-x64.exe
3f9b670c9e046e91f03b65fff4244ac5ebc90bd29d13583eca25691642b73b90  WZAI-1.0.1-linux-amd64.deb
b02242bda781665bbc4a3be17ffc5b02311b9a5c7682dbea97a36d06bfe992a8  WZAI-1.0.1-noplugin-linux-amd64.deb
579b637cd2781626313b82c07f8b91592674f99b4eeff754db632f409bb97598  WZAI-1.0.1-mac-x64.dmg
452d67e20bf42a934c682696084e559928a0d5c21a397a9ca183f8b7523baea8  WZAI-1.0.1-noplugin-mac-x64.dmg
```

每个安装包同时附有 `.sha256` 文件，供更新器自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\wzagent开发\<系统>\wzai-v1.0.1\`（插件版）与 `wzai-v1.0.1-noplugin\`（无插件版）

### 说明

- Windows 安装包未做代码签名；macOS 未做公证。
