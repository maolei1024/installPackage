# Vimium

- 扩展 ID：`dbepggeogbaibhgnhhndojpepiihcmeb`
- 版本：`2.4.2`（Manifest V3）
- 下载日期：2026-09-19
- [Chrome 网上应用店](https://chromewebstore.google.com/detail/dbepggeogbaibhgnhhndojpepiihcmeb)
- 来源：Google 官方扩展更新服务 `clients2.google.com/service/update2/crx`，由其重定向下载。

## 文件

- `vimium-2.4.2.crx`：官方原始扩展包，未修改。
- `vimium-2.4.2.zip`：从该 CRX 中直接提取的原始 ZIP 内容，方便解压安装。
- `SHA256SUMS`：以上文件的 SHA-256 校验值。

已验证 CRX3 签名、签名公钥对应的扩展 ID，以及 ZIP 内容的 CRC 完整性。

## 安装

优先通过上面的 Chrome 网上应用店链接安装，可获得商店自动更新。

离线安装可解压 ZIP，打开 `chrome://extensions/`，开启“开发者模式”，选择“加载已解压的扩展程序”，再选择包含 `manifest.json` 的解压目录。安装后请保留该目录。浏览器或组织策略可能限制离线安装；Chrome 通常限制直接拖入 CRX 安装。

在此目录运行 `sha256sum -c SHA256SUMS` 可校验下载文件。
