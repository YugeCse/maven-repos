# android-maven-repository
Android maven repositories. Github Maven仓库

<table style="text-align:center">
   <tr><th>名称</th><td>最新版本</td><td>修订日期</td></tr>
   <tr><td>Network</td><td>1.1.6</td><td>2023/12/04</td></tr>
   <tr><td>Common</td><td>1.1.6-1</td><td>2023/12/05</td></tr>
   <tr><td>Common-Compose</td><td>1.0.1</td><td>2023/10/26</td></tr>
   <tr><td>Shimmer</td><td>1.0.1</td><td>2023/11/27</td></tr>
   <tr><td>Image-Compressor</td><td>3.0.2</td><td>2023/12/06</td></tr>
</table>

## Common & Network & Tracking

- Common: 负责公共类、常用方法以及常用组件等内容；
- Network: 负责网络模块，使用 Okhttp+Retrofit+Coroutine；
- Tracking: 埋点处理类，负责埋点记录、埋点上传等工作；
- Common-Compose：依赖于Common库，需要Implementation("compose-foundation");

# 扩展库
- Shimmer: shimmer闪光Loading库，源自facebook:shimmer-android;
  集成方式：implementation("com.sg.android:shimmer") - 原包名保留
- Compressor: 图片压缩库，因原作者不再维护，Fork后的自己维护的版本。
  集成方式：implementation("com.sg.android:compressor") - 原包名保留

注意：集成需要配置以下内容到项目

1. 远程 Maven 集成：settings.gradle.kts
   ```kts
   maven {
       credentials {
           username = "username"
           password = "password"
       }
       isAllowInsecureProtocol = true
       url = uri("https://raw.githubusercontent.com/YugeCse/maven-repos/master/repo")
   }
   ```
2. 集成 maven 中第三方库
   引入 network 的 Maven
   ```kts
   implementation("com.squareup.okhttp3:okhttp:4.12.0") //okhttp //必选
   implementation("com.squareup.retrofit2:retrofit:2.9.0") //retrofit2 //必选
   implementation("com.squareup.retrofit2:converter-gson:2.9.0") //gson //必选
   implementation("com.jakewharton.retrofit:retrofit2-kotlin-coroutines-adapter:0.9.2") //必选
   implementation("org.jetbrains.kotlinx:kotlinx-coroutines-core:1.7.3") //必选
   implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:2.6.2") //必选
   implementation("androidx.lifecycle:lifecycle-runtime-ktx:2.6.2") //必选
   implementation("androidx.lifecycle:lifecycle-livedata-ktx:2.6.2") //必选
   implementation("com.sg.android:network:1.1.6")   //以上内容针对network是必选项，引入network的必须引入以上内容
   ```
   引入 common 的 Maven
   ```kts
   implementation("com.jakewharton.timber:timber:5.0.1") //必选
   implementation("androidx.webkit:webkit:1.8.0") //必选
   implementation("com.google.code.gson:gson:2.10.1") //必选
   implementation("com.tencent:mmkv:1.3.1") //必选
   implementation("org.greenrobot:eventbus:3.3.1") //必选，1.1.5及之后的不再是必选
   implementation("com.sg.android:common:1.1.6-1")   //以上内容针对common是必选项，引入network的必须引入以上内容
   ```

   引用 shimmer 的 Maven
   ```kts
   implementation("com.sg.android:shimmer:1.0.1")
   ```

# What's Changed?

+ **Network-v1.1.6** ； 2023/12/05 01:40pm
  + 公共库dimen资源增加806dpi和886dpi。

+ **Network-v1.1.6** ； 2023/12/04 05:00pm
  + 网络库Release模式下，接口请求前会判断网络有无。

+ **Common-v1.1.6** ； 2023/11/23 04:01pm
  + 删除多余的资源文件，新增数据流到文件的转换方法。

+ **Network-v1.1.5-4** ； 2023/11/03 05:30pm
  + 1.Network发布版本v1.1.5-4；
  + 2.修复文件下载器的进度通知问题。

+ **Common-v1.1.5** ； 2023/10/27 10:57am
  + 去掉EventBus的依赖。

