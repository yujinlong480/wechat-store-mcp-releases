# 微信小店数据工作台

微信小店数据工作台是一款面向微信小店经营者的 Windows 桌面辅助工具，用于汇总店铺经营、违规、预警和资金结算数据，并提供品退申诉、视频去重与 AI 能力。

本仓库是软件的唯一公开分发仓库，仅提供正式 Release，不包含源代码。

## 下载

请前往 [Releases](https://github.com/yujinlong480/wechat-store-mcp-releases/releases) 下载最新正式版本。

每个正式 Release 包含：

- `WeChatStoreWorkbench-v1.0.15-portable.zip`
- `WeChatStoreWorkbench-v1.0.15-portable.zip.sha256`

## 便携版使用

1. 下载 ZIP 和对应的 `.sha256` 文件。
2. 校验 ZIP 的 SHA-256。
3. 将 ZIP **完整解压**到可写目录，不要直接在压缩包内运行。
4. 双击解压目录中的 `WeChatStoreWorkbench-v1.0.15.exe`。
5. 不要只复制 EXE；`runtime` 目录包含视频处理和自定义方案所需组件。
6. 首次运行会在 EXE 同目录创建 `data`，业务数据默认仅保存在本机。

```text
WeChatStoreWorkbench-v1.0.15-portable/
  WeChatStoreWorkbench-v1.0.15.exe
  README.txt
  LICENSE
  THIRD_PARTY_NOTICES.txt
  runtime/
    ffmpeg/
    python/
```

## 浏览器要求

便携包不内置浏览器。电脑必须安装以下任一浏览器：

- Microsoft Edge：https://www.microsoft.com/edge
- Google Chrome：https://www.google.com/chrome/

如果软件未检测到可用浏览器，会显示安装提示和下载入口。安装后点击“重新检测”或重新启动软件。

## 校验下载文件

```powershell
$zip = '.\WeChatStoreWorkbench-v1.0.15-portable.zip'
(Get-FileHash -LiteralPath $zip -Algorithm SHA256).Hash.ToLowerInvariant()
Get-Content -LiteralPath "$zip.sha256"
```

两处 SHA-256 应完全一致。校验不一致时请勿解压运行。

## 一键升级

软件左下角提供“一键升级”。升级时会校验 Release 中的便携 ZIP：

- 替换程序 EXE
- 替换 `runtime` 运行组件
- 保留 `data` 业务数据
- 升级失败时尝试恢复旧版本运行目录

## 数据迁移

迁移电脑时复制整个 `data` 文件夹。微信登录凭证使用 Windows DPAPI 加密，换电脑后通常需要重新登录；抖音和 AI 账号也建议重新登录。

## 隐私说明

本仓库不接收店铺名称、微信账号、登录凭证、经营金额或保证金数据。软件仅在用户开启匿名统计时上报匿名安装 ID、日期、版本、启动次数和同步次数；业务数据默认只存储在本机。

## 系统要求

- Windows 10 或 Windows 11，64 位
- Microsoft Edge 或 Google Chrome
- 首次登录和同步时需要访问微信小店网页
- 视频去重需要访问抖音
- AI 功能需要访问 CloudBase
- 一键升级需要访问 GitHub Releases

## 许可

软件本体采用 [Proprietary Freeware License 1.0](LICENSE)。软件可免费使用，但源代码不公开，未经授权不得复制、修改、反向工程或再分发。

ffmpeg、Python、Playwright 等第三方组件分别遵循其自身许可证，完整说明见发布 ZIP 内的 `THIRD_PARTY_NOTICES.txt`。

## 联系

微信：`xyz0553`

软件基础功能永久免费，欢迎提交使用反馈，也支持定制开发。
