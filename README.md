# android-maven-repository
Android maven repositories. Github Maven仓库

<table style="text-align:center">
   <tr><th width="30%" style="text-align:left">名称</th><td width="30%">最新版本</td><td>修订日期</td><td>修订人</td></tr>
   <tr><td style="text-align:left">Network</td><td>1.8.0</td><td>2024/03/19</td><td>Hwang</td></tr>
   <tr><td style="text-align:left">Common</td><td>1.8.0</td><td>2024/05/15</td><td>Hwang</td></tr>
   <tr><td style="text-align:left">Common-Compose</td><td>1.8.0</td><td>2024/05/15</td><td>Hwang</td></tr>
   <tr><td style="text-align:left">Tracking</td><td>1.8.2</td><td>2024/06/11</td><td>Hwang</td></tr>
   <tr><td style="text-align:left">ABTest</td><td>1.8.1</td><td>2024/06/11</td><td>Hwang</td></tr>
</table>

# What's Changed?

- **Tracking-v1.8.2** ； 2024/06/11 09:19am
  - 升级埋点sdk，增加数据上传时倒序还是顺序查询；
  - gradle升级到8.4.2，from 8.2.2

- **ABTest-v1.8.1** ； 2024/06/11 09:19am
  - 升级埋点sdk，增加数据上传时倒序还是顺序查询；
  - gradle升级到8.4.2，from 8.2.2

- **Common/Network/Common-Compose/Tracking/ABTesting** ； 2024/05/15
  - 升级一些第三方库，所有sdk升级到1.8.0

- **Common-v1.1.9** ； 2024/03/27 11:30am

    - 增加ppi409的设备适配：vivo-s10

- **Network-v1.1.9** ； 2024/03/19 03:30am

    - 网络库Retrofit升级：2.9.0->2.10.0

- **Tracking-v1.0.7** ； 2024/03/11 04:30am

    - Tracking 库 发布v1.0.8
    - 页面停留参数：增加screen_id和page_name

- **Common-v1.1.8** ； 2024/03/06 12:00

    - ShareUtils类增加try-catch安全机制

- **Network-v1.1.8** ； 2024/03/06 12:00

    - 网络库ContextProvider类调整修改

- **ABTest-v1.0.4** ； 2024/03/01 11:00am

    - ABTest 库 发布v1.0.4
    - 优化网络上传问题

- **Tracking-v1.0.7** ； 2024/03/01 11:00am

    - Tracking 库 发布v1.0.7
    - 优化网络上传问题

- **Common-v1.1.6-2** ； 2024/01/16 17:20pm

  - Common 库 发布v1.1.6-2
  - 1. 新增适配ppi429的设备 - dimens-xml-added
  - 2. FontSizeSeekBar开放一些属性方法。

- **ABTest-v1.0.2** ； 2024/01/09 16:20pm

  - ABTest 库 发布v1.0.2
  - 1. 优化GETSSID方法。
  - 2. 增加SSID配置类，方便参数配置。

- **Tracking-v1.0.5** ； 2024/01/09 16:20pm

  - Tracking 库 发布v1.0.5
  - 1. 优化GETSSID方法。

- **ABTest-v1.0.1** ； 2024/01/08 17:40pm

  - ABTest 库 发布v1.0.1
  - 1. 优化参数配置；
  - 2. 调整http-api逻辑。

- **Tracking-v1.0.4** ； 2024/01/08 17:40pm

  - Tracking 库 发布v1.0.4
  - 1. 优化参数配置；
  - 2. 调整http-api逻辑。

- **Tracking-v1.0.3** ； 2024/01/08:40pm

  - Tracking 库 发布v1.0.3
  - 1. 优化网络访问状态码判断逻辑；
  - 2. 调整http-api逻辑。

- **Tracking-v1.0.2** ； 2024/01/04:40pm

  - Tracking 库 发布v1.0.2

- **Tracking-v1.0.0** ； 2024/01/05 09:40pm

  - Tracking 库 发布v1.0.0

- **Common-v1.1.6-1** ； 2023/12/05 01:40pm

  - Common 库 dimen 资源增加 806dpi 和 886dpi。

- **Network-v1.1.6** ； 2023/12/04 05:00pm

  - 网络库 Release 模式下，接口请求前会判断网络有无。

- **Common-v1.1.6** ； 2023/11/23 04:01pm

  - 删除多余的资源文件，新增数据流到文件的转换方法。

- **Network-v1.1.5-4** ； 2023/11/03 05:30pm

  - 1.Network 发布版本 v1.1.5-4；
  - 2.修复文件下载器的进度通知问题。

- **Common-v1.1.5** ； 2023/10/27 10:57am
  - 去掉 EventBus 的依赖。