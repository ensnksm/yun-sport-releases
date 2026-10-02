# 云运动个人版发布

此仓库用于发布安装包与签名更新清单。Windows 客户端、Windows 卡密管理器、安卓客户端、安卓卡密管理器采用同一发布批次，当前同步协议为 3。

当前共同版本为 [0.1.2](https://github.com/ensnksm/yun-sport-releases/releases/tag/v0.1.2)。安卓客户端已在真机从 0.1.0 经软件内更新升级到 0.1.2；手机管理器实际连接电脑并显示真实绑定账号。学校账号完整登录与跑步流程尚未在手机版验收。

## 安装与更新

从 [Releases](https://github.com/ensnksm/yun-sport-releases/releases) 下载对应文件。第一次需要手动安装带更新功能的版本，以后可在程序内检查更新。APK 仅支持 Android 10 及以上的 ARM64 手机；iPhone 原生版尚未发布。

安卓安装更新需要系统确认。Windows 更新保留授权数据，保留一份旧 EXE；运行任务期间延后安装。

手机卡密管理器是发卡电脑的管理助手。导入自己的管理员授权文件后，可在发卡电脑在线时查询账号绑定、生成和撤销卡密；不要把管理员授权文件发给别人。普通客户端 APK 不包含发卡私钥。

旧 Windows 发布文件保留；要使用手机管理功能，需要更新发卡电脑的管理器。管理器 EXE 应放在原 `license_service` 目录的子文件夹中，以便使用原 `state` 数据。不要创建空数据库替代原数据。

## 网络与安全

GitHub 提供安装包下载；卡密验证仍由互联电脑完成。国内网络访问 GitHub 的情况不同，不保证任意 Wi-Fi 能下载或连接到所有节点。

更新清单使用单独的 Ed25519 发布签名，客户端下载后校验大小和 SHA-256。APK 使用固定 RSA 应用签名并启用 R8。混淆和本地校验不能保证客户端永远无法被修改；发卡私钥和管理权限在可信端校验。

管理员密钥、卡密数据库、账号密码、登录 Token 和手机管理员授权文件均不发布到此仓库。

## 项目来源

学校业务逻辑基于 [Zirconium233/yunForNewVersion](https://github.com/Zirconium233/yunForNewVersion)。本仓库不是原作者维护的官方仓库。联网使用 Hyperswarm、Autobase、Corestore、Hyperbee、Protomux；安卓运行时使用 Bare Kit 和 Chaquopy。
