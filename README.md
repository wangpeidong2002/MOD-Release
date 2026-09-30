# MOD-Release

MOD Rhino 插件的公开、匿名更新分发仓库。这里只保存可安装的发布文件，不包含项目源码、调试符号或授权名单。

## 下载与安装

当前版本：**MOD 1.0.100**（2026-09-30）。

- [下载完整安装器](https://raw.githubusercontent.com/wangpeidong2002/MOD-Release/main/Release/MODInstaller-1.0.100.exe)
- [下载完整安装包](https://raw.githubusercontent.com/wangpeidong2002/MOD-Release/main/Release/MOD-package-1.0.100.zip)
- [版本说明](https://github.com/wangpeidong2002/MOD-Release/releases/tag/v1.0.100)

旧版升级建议运行完整安装器，同步外壳、核心与运行依赖。保存模型后关闭 Rhino，再完成安装；安装器不会强制关闭 Rhino。手动安装请完整解压 ZIP，并保留所有相对目录。

## 固定更新路径

- 当前完整更新清单：`Release/bundle-v2-latest.json`
- 兼容完整更新清单：`Release/bundle-latest.json`
- 兼容核心更新清单：`Release/latest.json`
- 签名核心：`Release/MODCreo.dll`

客户端只接受本仓库 `main` 分支下的固定 GitHub Raw 地址，并验证 RSA-PSS 签名、文件大小及 SHA-256。

## 发布约束

- `latest.json` 中的 SHA-256 必须与同目录的 `MODCreo.dll` 完全一致。
- 不要改名或移动 `Release`、`latest.json`、`MODCreo.dll`。
- 完整安装时必须保留 DLL、JSON、`EmbeddedResource` 与 `runtimes` 的相对目录结构。
- 版本化 ZIP/EXE 发布后不可覆盖；固定清单与对应文件须在同一次提交中更新。
- `latest.json` 保留旧版核心更新兼容；涉及外壳或依赖的升级请使用完整安装器或 ZIP。
