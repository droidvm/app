在虚拟电脑APP中安装其它的Linux发行版

<b>特别说明：</b><br>
　　正卓软件管家<b>仅可用于</b>ubuntu系统，<br>
　　其它发行版仅供专业玩家安装体验，<br>
　　请自行研究！<br>

虚拟电脑app版本：<br>
　　1.38，或以上，建议使用最新版。

实现方式为：
　　在虚拟系统的安装界面<br>
　　自动识别剪贴板的内容是否以：<br>
　　"zzvm://" 开头。<br>
<br>

<b>具体步骤如下：</b><br>
第一步：<br>
　　卸载虚拟电脑app、重新安装，但先不要启动<br>
　　或者，把虚拟电脑app的存储清空<br>
　　或者，开始->控制台->系统->重新安装系统<br>
<br>
　　第一步操作完后 【【 先不要 】】 启动！<br>
<br>
第二步：<br>
　　点击下边绿色按钮，选好发行版，<br>
　　并复制对应的安装口令(无需粘贴到终端运行)<br>
<br>
第三步：<br>
　　启动虚拟电脑app (虚拟系统的安装界面)<br>
<br>
<br>

<b>目前支持的安装口令如下：</b>

Ubuntu 24.04, 全新安装
```
zzvm://setup
```


Ubuntu 26.04, 全新安装
```
zzvm://rootfs
arch=arm64
genv=1
info="ubuntu官方仓库"
dist=ubuntu
code=26.04
name=raccoon
uzip=-xzf
fzip=ubuntu-base-26.04-base-arm64.tar.gz
addr=https://cdimage.ubuntu.com/ubuntu-base/releases/26.04/release/$fzip
```
