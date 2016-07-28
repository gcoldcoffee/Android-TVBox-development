# 安卓智能盒子开发
##盒子开发与手机区别
- 分辨率
- 性能
- 事件

##开发工具与盒子联机调试示例 Window系统示例

- 安装好开发工具，配置 adb 环境命令[百度操作示意](http://jingyan.baidu.com/article/17bd8e52f514d985ab2bb800.html)
- 打开系统cmd命令窗口，通过adb connect ip。 ip 为需要连接的盒子，是否连接成功 cmd命令行窗口有对应提示。
- adb devices 可查看已连接的所有设备

##很好的demo
- [本人做过的应用，请安装到安卓智能盒子或者电视](https://github.com/gcoldcoffee/Android-TVBox-development/blob/master/KanKeHD%2B.apk)
- [据说东半球最好的TV桌面开源项目](http://blog.csdn.net/rain_butterfly/article/details/44942747)

##adb 常用相关命令
- [点击查看命令文档](https://github.com/gcoldcoffee/Android-TVBox-development/blob/master/adb%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4.txt)
- adb connect   ip 连接设备
- adb devices   查看已连接设备
- adb start-server    启动adb服务
- adb kill-server   关闭服务
- adb install //file:text.apk   安装应用
- adb uninstall packName    卸载应用

####adb启动activity:
  adb shell<br/>
  am start -n ｛包(package)名｝/｛包名｝.{活动(activity)名称}<br/>
  如：启动浏览器<br/>
  am start -n com.android.browser/com.android.browser.BrowserActivity<br/>

####adb启动service:
  adb shell<br/>
  am startservice -n ｛包(package)名｝/｛包名｝.{服务(service)名称}<br/>
  am startservice --user 0 -n ｛包(package)名｝/｛包名｝.{服务(service)名称}<br/>

####adb发送broadcast:
   adb shell<br/>
   am broadcast -a <广播动作><br/>
   如：发送一个网络变化的广播<br/>
   am broadcast -a android.net.conn.CONNECTIVITY_CHANGE<br/>
  
####获取设备已安装列表:
  adb -s ip:5555 shell pm list packages

##adb 相关资料
-[资料](https://github.com/gcoldcoffee/Android-TVBox-development/blob/master/%E8%B5%84%E6%96%99URL.txt)


# 我的QQ，有疑问可加我
![image](https://github.com/gcoldcoffee/Android-TVBox-development/blob/master/qq.png)
