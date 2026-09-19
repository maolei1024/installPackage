# ChatGPT（原 Codex）Windows x64 离线安装

[下载本仓库离线安装附件](https://github.com/maolei1024/installPackage/releases/tag/codex-26.915.4065.0-windows-x64-offline)

- 包版本：`26.915.4065.0`
- 显示名称：ChatGPT；包标识：`OpenAI.Codex`
- 系统：x64，Windows 10 2004（内部版本 19041）或更新版本，包括 Windows 11；这是包清单声明的最低版本。
- MSIX 大小：824,570,408 字节（约 786 MiB）
- 下载日期：2026-09-19
- 完整 MSIX 保存在 Releases，因其超过普通 Git 文件大小限制。

## 下载并带入内网

从上面的 Release 下载 `ChatGPT-x64.msix`、`ChatGPT-License.xml`、`SHA256SUMS` 和本说明 `README.md`，复制到内网 Windows 电脑的同一个文件夹。无需之前的在线安装器 `CodexInstaller.exe`。

## 安装

在该文件夹打开**管理员 Windows PowerShell**，先检查文件校验值：

```powershell
Get-FileHash .\ChatGPT-x64.msix -Algorithm SHA256
Get-FileHash .\ChatGPT-License.xml -Algorithm SHA256
```

将结果与 `SHA256SUMS` 中对应文件的值比较。然后运行官方文档采用的预配安装命令：

```powershell
Add-AppxProvisionedPackage -Online -PackagePath .\ChatGPT-x64.msix -LicensePath .\ChatGPT-License.xml -Regions all
```

这里的 `-Online` 指操作当前运行的 Windows 系统，而不是要求联网下载安装包。如果开始菜单未显示应用，注销 Windows 后重新登录。

包清单没有声明额外的 `PackageDependency` 框架包；目标电脑仍需正常可用的 Windows 应用部署组件及允许此类安装的组织策略。未在实际内网 Windows 设备上执行安装验证。

## 使用限制

**离线安装不等于离线 AI 使用。** 官方文档明确说明离线安装不提供 ChatGPT 离线访问。如果设备无法访问所需的认证及模型服务，仅安装此包不能实现断网使用云端 AI。本安装包不包含本地模型。

## 来源与验证

- [OpenAI 官方 Windows 部署说明](https://developers.openai.com/codex/enterprise/windows-deployment)
- [官方 x64 MSIX](https://persistent.oaistatic.com/codex-app-prod/ChatGPT-x64.msix)
- [官方离线许可证](https://persistent.oaistatic.com/codex-app-prod/ChatGPT-License.xml)

官方说明这些链接提供 Store 签名包。文件未修改，已检查 ZIP CRC 完整性、包清单及签名文件存在；未在 Windows 上验证签名信任链或实际安装。SHA-256 是本次下载后计算的副本校验值，并非另行取得的官方哈希。

MSIX SHA-256：`fb4745f5378c8a4122f74643a3c7c1000da5f4b184f0d9dc9faf275c79ac73a4`。
