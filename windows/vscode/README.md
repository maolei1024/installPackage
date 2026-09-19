# Visual Studio Code for Windows

- 版本：1.138.0 Stable
- 平台：Windows x64，User Setup（当前用户安装）
- 下载日期：2026-09-19
- 文件大小：236,054,360 字节
- [下载安装包](https://github.com/maolei1024/installPackage/releases/download/vscode-1.138.0-windows-x64/VSCodeUserSetup-x64-1.138.0.exe)
- [官方版本元数据](https://update.code.visualstudio.com/api/update/win32-x64-user/stable/latest)

安装包超过 GitHub 普通 Git 文件的 100 MiB 限制，因此保存在本仓库 Releases。下载 EXE 后双击安装。

已核对文件 SHA-256 与 Microsoft 官方元数据一致。`upstream-metadata.json` 保存本次下载的版本和原始下载地址，`SHA256SUMS` 保存校验值。

PowerShell 校验命令：

```powershell
Get-FileHash .\VSCodeUserSetup-x64-1.138.0.exe -Algorithm SHA256
```

期望 SHA-256：`820df7a601d0179fc850433e1a1c047d2926a7a5a78ef01cd49fe8833fa2010d`。
