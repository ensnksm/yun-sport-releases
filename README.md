# 云运动个人版发布

此仓库仅发布 Windows 与安卓云运动客户端及签名更新清单，当前同步协议为 3。卡密管理器仅由所有者在本机保留和维护。

当前版本从 [最新发布](https://github.com/ensnksm/yun-sport-releases/releases/latest) 获取。安卓客户端的软件内更新已真机验证；学校账号完整登录与跑步流程尚未在手机版验收。

## 安装与更新

从 [Releases](https://github.com/ensnksm/yun-sport-releases/releases) 下载对应文件。第一次需要手动安装带更新功能的版本，以后可在程序内检查更新。APK 仅支持 Android 10 及以上的 ARM64 手机；iPhone 原生版尚未发布。

安卓安装更新需要系统确认。Windows 更新保留授权数据，保留一份旧 EXE；运行任务期间延后安装。

公开文件严格限于 `android-client.apk`、`windows-client.exe`、`updates.json`、`SHA256SUMS.txt`。三个历史版本的卡密管理器附件已撤下，更新清单只含云运动客户端。

登录并通过授权登记的手机客户端可以在后台与电脑互联，按照同一授权与共同确认规则协助核验。后台联网保留系统通知，手机省电策略和网络状态可能影响持续在线。

## 网络与安全

GitHub 提供安装包下载；卡密验证仍由互联电脑完成。国内网络访问 GitHub 的情况不同，不保证任意 Wi-Fi 能下载或连接到所有节点。

更新清单使用单独的 Ed25519 发布签名，客户端下载后校验大小和 SHA-256。APK 使用固定 RSA 应用签名并启用 R8。混淆和本地校验不能保证客户端永远无法被修改；发卡私钥和管理权限在可信端校验。

管理员密钥、卡密数据库、账号密码、登录 Token 和手机管理员授权文件均不发布到此仓库。

## 项目来源

学校业务逻辑基于 [Zirconium233/yunForNewVersion](https://github.com/Zirconium233/yunForNewVersion)。本仓库不是原作者维护的官方仓库。联网使用 Hyperswarm、Autobase、Corestore、Hyperbee、Protomux；安卓运行时使用 Bare Kit 和 Chaquopy。
