# 多平台发布视频逆向代码实现 (2025年2月份最新版)

各平台的发布视频代码均通过 Python 实现，Python 版本 3.10+，不基于 headless browser，全部通过调接口实现，执行效率更高，风控风险更小。

## 一、抖音
1. 登录创作者平台，拷贝出 cookie，以及此时浏览器 local storage 里的 `security-sdk/s_sdk_crypt_sdk` 中的 `ec_privateKey`，还有 `security-sdk/s_sdk_sign_data_key/web_protect` 里的 `ts_sign`；
2. 上述的 `privateKey` 和 `ts_sign` 用于计算 `/web/api/media/aweme/create/` 接口里的 `bd-ticket-guard-client-data` 参数和 `bd-ticket-guard-ree-public-key` 参数；
3. 支持视频切片、上传、发布全流程，实测 40MB 视频全流程耗时约 10 秒（取决于执行代码所在的网络环境）；
4. 如需其他语言的版本，可额外开发提供（可支持 Java、PHP、Golang、NodeJS 等）；

## 二、视频号
1. 登录视频号助手，拷贝出 cookie；
2. 基于提供的 Python 代码，可以挂指定的任意城市的 POI（假设您在上海，可以挂北京的 POI）；
3. 支持视频切片、上传、发布全流程；
4. 如需其他语言的版本，可额外开发提供（可支持 Java、PHP、Golang、NodeJS 等）；

## 三、小红书
1. 登录小红书创作服务平台，拷贝出 cookie；
2. 提供 `xs`、`xt` 的计算源码；
3. 提供本地 `a1` 的生成源码；
4. 支持视频切片、上传、发布全流程；
5. 如需其他语言的版本，可额外开发提供（可支持 Java、PHP、Golang、NodeJS 等）；

## 四、快手
1. 登录快手创作者服务平台，拷贝出 cookie；
2. 提供 `ns_sig3` 签名算法；
3. 支持视频切片、上传、发布全流程；

# 客户端体验下载链接

- **macOS ARM芯片**：[MatriX-Lite 0.4.5 ARM64](https://sense-video.oss-cn-hangzhou.aliyuncs.com/wsb/matrix/MatriX-Lite-0.4.5-arm64.dmg)
- **macOS Intel芯片**：[MatriX-Lite 0.4.5 X64](https://sense-video.oss-cn-hangzhou.aliyuncs.com/wsb/matrix/MatriX-Lite-0.4.5-x64.dmg)
- **Windows**：[MatriX-Lite 0.4.5 X64 Setup](https://sense-video.oss-cn-hangzhou.aliyuncs.com/wsb/matrix/matrix-lite-0.4.5-x64-setup.exe)
## 客户端使用说明文档
[使用说明文档](https://hcnspeemjow3.feishu.cn/docx/Qo1cdvG3nogIRVx6BYkcdTpsn8b)

# 联系我

如果对上述技术感兴趣，可以加WX `wfeifan0` 欢迎咨询交流～
