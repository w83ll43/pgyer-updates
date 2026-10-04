# 蒲公英软件更新

集中管理各软件的公开更新元数据，按软件分目录；安装包由蒲公英分发。

## 软件

| 软件 | 最新版本订阅 | 安装页 |
| --- | --- | --- |
| 拾器 PocketKit | [release.json](https://raw.githubusercontent.com/w83ll43/pgyer-updates/main/apps/pocketkit/release.json) | [蒲公英](https://www.pgyer.com/shiqi-ios) |

## 目录与接入

- `apps/<app-id>/release.json`：最近一次实际发布的版本。客户端固定使用自己软件的 HTTPS 地址。
- `apps/<app-id>/releases/<version>-<build>.md`：已发布说明，不覆盖历史。
- `schema/release.schema.json`：各软件共用的字段约定。新增软件使用小写字母、数字和短横线的独立 ID。

发布器在蒲公英确认安装包发布成功后，更新对应软件的文件；不要提前写入计划版本。版本和构建号必须与实际 IPA 一致。其他软件只写自己的目录，不能覆盖拾器订阅。

更新说明默认 3–5 条，一条一句“新增／优化／修复”，只写用户可见的变化；必要的实验或兼容性限制用短句保留。技术验证留在各自源码仓库。

本仓库不保存源码、IPA、证书、API Key、安装密码或设备凭据。安装链接只使用蒲公英官方安装页或官方 manifest 链接。

## 拾器旧版兼容

`w83ll43/PocketKit-updates` 的根目录订阅继续同步相同发布元数据，为旧版拾器提供更新。新客户端不再提供手动填写更新地址。客户端变化要随新的安装包发布才会生效；本仓库不会替换设备上的 App。
