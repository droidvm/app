解除安卓进程数限制<br>
虚拟电脑app是个多进程应用，进程解限后才能稳定运行。<br>
<br>

为了省电，在使用电池的设备上安卓系统会：
1. 随机结束处于后台运行的应用进程。
2. 熄屏后前台应用进程可能也会杀掉
<br>
也就是 "杀进程"，多进程应用需要防杀、保活。
<br>

进程解限的步骤：<br>
(部分安卓机型中自带 "停止限制子进程" 的开关, 可省掉以下繁琐操作)<br>

第一步，在手机上“开发者模式”启用
1. 手机上点开“设置”
2. 设置界面拉到最底部，点击“关机本机”
3. 点击“版本信息”
4. 连续点击“版本号”10次，即可开启手机的“开发者模式”

第二步，在手机上将“USB调试”开关打开
1. 手机上点开“设置”
2. 设置界面拉到最底部，点击“系统设置”
3. 拉到最底部，点击“开发者选项”
4. 慢慢下拉，找到“USB调试”这一项，将开关打开即可。

第三步，在电脑上adb指令连上手机, 然后运行如下指令：
```
adb shell device_config set_sync_disabled_for_tests persistent
adb shell device_config put activity_manager max_phantom_processes 65536
adb shell dumpsys activity settings | grep max_phantom_processes
adb shell settings put global settings_enable_monitor_phantom_procs false
```
以下两种情况可以使用软件管家中的adbme替代电脑:
1. 在支持无线调试的设备上, 此时 adbme 走 tcp-adb
2. 有 usb对联线+两安卓机, 此时 adbme 会通过 usb-adb 先打开 tcp-adb 通道
<br>
<br>
[adbme 视频教程：不借助电脑，只用手机实现adb自连](https://www.bilibili.com/video/BV1PS421w7Tv/)
<br>
<br>

【注】
```
手机重启后
需要重做第二步和第三步
进行重新解限。
```
