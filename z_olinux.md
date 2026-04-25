在虚拟电脑APP中安装其它的Linux发行版

<b>特别说明：</b><br>
　　正卓软件管家<b>仅可用于</b>ubuntu系统，<br>
　　其它发行版仅供专业玩家安装体验，<br>
　　故安装过程上遇到问题<b>请自行研究解决！</b><br>
　　安装脚本参考: https://gitee.com/droidvm/linux-installer-for-droidvm/tree/master/distributions<br>
<br>

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
　　复制对应的安装口令(无需粘贴到终端运行)<br>
　　启动虚拟电脑app (虚拟系统的安装界面会识别口令)<br>
<br>
<br>

<b>目前支持的安装口令如下：</b>

(deb系) Ubuntu 24.04, 全新安装
```
zzvm://setup
```


(deb系) Ubuntu 26.04, 全新安装
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

(deb系) Deepin默认rootfs
```
zzvm://rootfs
dist=deepin
arch=arm64
genv=1
# https://github.com/deepin-community/deepin-rootfs/releases
# 1.4.0
```

(deb系) Deepin自定义rootfs
```
zzvm://rootfs
arch=arm64
genv=1
info="github仓库"
dist=deepin
code=4.0.2
name=beige
uzip=-xf
fzip=deepin-rootfs-arm64.tar.gz
addr=http://192.168.1.5/$fzip
# 请自行替换下载链接
```

(deb系) Debian默认rootfs
```
zzvm://rootfs
dist=debian
arch=arm64
genv=1
# https://mirrors.tuna.tsinghua.edu.cn/lxc-images/images/debian/trixie/
# https://images.linuxcontainers.org/images/debian/
# 13.1.0 (trixie)
```

(deb系) Debian自定义rootfs
```
zzvm://rootfs
arch=arm64
genv=1
info="自定义下载地址"
dist=debian
code=13.1.0
name=trixie
uzip=-xJf
fzip=lxc_debian-13.1.0-arm64.tar.xz
addr=http://192.168.1.5/apps/droidvm/downloads/$fzip
# 请自行替换下载链接
```

(deb系) kali默认rootfs
```
zzvm://rootfs
dist=kali
arch=arm64
genv=1
# https://images.linuxcontainers.org/images/kali/current/arm64/default/
# 滚动更新版
```

(arch系) GXDE-OS默认rootfs
```
zzvm://rootfs
dist=gxde-os
arch=arm64
genv=1
# rootfs: https://mirrors.sdu.edu.cn/spark-store/GXDE-OS/TGZ/debian-gxde.tar.xz.rootfs
```

(rpm系) openeuler默认rootfs
```
zzvm://rootfs
dist=openeuler
arch=arm64
genv=1
# https://mirrors.tuna.tsinghua.edu.cn/lxc-images/images/openeuler/24.09/arm64/default/
# 24.09
```

(arch系) archlinux默认rootfs
```
zzvm://rootfs
dist=archlinux
arch=arm64
genv=1
```

