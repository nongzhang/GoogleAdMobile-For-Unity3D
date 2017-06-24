# GoogleAdMobile-For-Unity3D
为你的游戏加入谷歌广告（包括横幅广告和插页式广告）

第一步.打开谷歌广告官网https://www.google.com/admob/, 注册一个账号或直接用谷歌账号登录.（需正确上网）
![Image](https://raw.github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.1.png)
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.1.png)

点击添加应用之后出来如下页面，如果已将应用发布到google play或app store则选是，否则选否.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.2.png)

继续回出现四种广告类型，这里选择第一个横幅广告.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.3.png)

选择之后会出现横幅广告的一些基本设置，这里取名为"首页广告"并保存.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.4.png)

至此，横幅广告就创建好了，记住广告单元ID,脚本中会用到.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.5.png)

第二步.在你的项目中添加广告.

打开https://developers.google.com/mobile-ads-sdk/docs/games#unity_plugin_api  下载适配unity的SDK（页面向下拉，这里会看到Android IOS Unity）
点击下载插件转到 https://github.com/googleads/googleads-mobile-unity/releases/tag/3.5.0 最新版本是3.5.0
导入到工程中如下图.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.6.png)

在开发者页面 https://developers.google.com/mobile-ads-sdk/docs/games 有横幅广告和插页式广告的示例代码，同理编写脚本GoogleAdManager并挂在到摄像机.

完成之后在unity中运行工程，若出现如下信息则广告基本没什么问题（注意，这是在unity运行环境而非实际安卓操作环境，故广告不显示）
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.7.png)

第三步.将工程编译为APK文件上机测试.
unity切换到Android平台，点开Player Setting，基本设置如下，这里使用的时Android4.0，确保你的Android SDK版本一致.
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.8.png)

若出现如下报错
ResolutionException: Cannot find candidate artifact for com.android.support:support-v4:25.2.0
Google.JarResolver.PlayServicesSupport.GetDependencies (Google.JarResolver.Dependency dep, System.Collections.Generic.List`1 repoPaths)
Google.JarResolver.PlayServicesSupport.GetTransitiveDependencies (System.Collections.Generic.Dictionary`2 dependencies, System.Collections.Generic.List`1 repoPaths)
Google.JarResolver.PlayServicesSupport.FindMissingDependencyPaths (System.String destinationDirectory, System.Collections.Generic.Dictionary`2& dependencyPaths, Google.JarResolver.ExplodeAar explodeAar)
GooglePlayServices.ResolverVer1_1.DoResolution (Google.JarResolver.PlayServicesSupport svcSupport, System.String destinationDirectory, Google.JarResolver.OverwriteConfirmation handleOverwriteConfirmation, System.Action resolutionComplete)
GooglePlayServices.PlayServicesResolver.Resolve (System.Action resolutionComplete)
GooglePlayServices.PlayServicesResolver.AutoResolve ()
UnityEditor.EditorApplication.Internal_CallUpdateFunctions () (at C:/buildslave/unity/build/artifacts/generated/common/editor/EditorApplicationBindings.gen.cs:217)


请将你的Android Support Repository和Google Repository升级到最新版本.(如下图)
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.9.png)

打包成功后测试。广告出现
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.10.png)
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.11.png)
![image](http://github.com/nongzhang/GoogleAdMobile-For-Unity3D/raw/master/GuideImage/1.12.png)
