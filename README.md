# MOD-Release

MOD Rhino 插件的公开、匿名更新分发仓库。这里只保存可安装的发布文件，不包含项目源码、调试符号或授权名单。

## 固定更新路径

- 清单：`Release/latest.json`
- 自动更新核心：`Release/MODCreo.dll`
- 完整安装包：`Release/`

客户端只接受本仓库 `main` 分支下的上述 GitHub Raw 地址，不读取本机自定义源、私有仓库或备用镜像。

## 发布约束

- `latest.json` 中的 SHA-256 必须与同目录的 `MODCreo.dll` 完全一致。
- 不要改名或移动 `Release`、`latest.json`、`MODCreo.dll`。
- 完整安装时必须保留 `Release` 内 DLL、JSON 与 `runtimes` 的相对目录结构。
- 自动更新当前只替换 `MODCreo.dll`；更新外壳或依赖时应重新部署完整 `Release` 文件夹。
