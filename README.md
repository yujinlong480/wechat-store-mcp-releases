# 微信小店数据工作台

微信小店数据工作台是一款面向微信小店经营者的 Windows 桌面辅助工具，用于汇总店铺经营、违规、预警和资金结算数据，并提供品退申诉与后续 AI 创作能力。

本仓库是软件的唯一公开分发仓库，仅提供正式 Release，不包含源代码。

## 下载

请前往 [Releases](https://github.com/yujinlong480/wechat-store-mcp-releases/releases) 下载最新正式版本。

每个正式 Release 包含：

- `WeChatStoreWorkbench-v1.0.11.exe`
- `WeChatStoreWorkbench-v1.0.11.exe.sha256`

## 校验下载文件

下载 EXE 和对应的 `.sha256` 文件后，在 PowerShell 中执行：

```powershell
$exe = '.\WeChatStoreWorkbench-v1.0.11.exe'
(Get-FileHash -LiteralPath $exe -Algorithm SHA256).Hash.ToLowerInvariant()
Get-Content -LiteralPath "$exe.sha256"
```

两处 SHA-256 应完全一致。校验不一致时请勿运行文件。

## 使用说明

1. 从 Releases 下载并运行 EXE。
2. 根据软件内提示登录微信小店账号。
3. 店铺、账号、金额、违规和同步数据默认仅保存在本机。
4. 软件支持从本公开仓库的正式 Release 检查并执行一键升级。
5. AI 功能使用邮箱验证码登录，非 AI 功能无需注册即可使用。

软件基础功能永久免费。AI 云端能力按积分计费，新用户提供可配置免费额度。欢迎提交使用反馈，也支持定制开发。

## 隐私说明

本仓库不接收店铺名称、微信账号、登录凭据、经营金额或保证金数据。软件仅在用户开启匿名统计时上报匿名安装 ID、日期、版本、启动次数和同步次数；业务数据保存在本机。

## 系统要求

- Windows 10 或 Windows 11，64 位
- 首次登录和同步时需要能够访问微信小店网页
- 一键升级需要能够访问 GitHub Releases

## 许可

本项目采用 [Proprietary Freeware License 1.0](LICENSE)。软件可免费使用，但源代码不公开，未经授权不得复制、修改、反向工程或再分发。

## 联系

微信：`xyz0553`
