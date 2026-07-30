#### zzwl 介绍
wayland服务端, 负责合成程序画面并送显<br>
未完善到可用的程度, 体验步骤: <br>echo "droidvm-zzwl">$app_home/app_boot_config/gui_srv_libname.txt

#### zzde 介绍
wayland客户端, 实现的是超小型桌面环境<br>
未完善到可用的程度

#### virvk 介绍
virvk 是 virglrenderer 中的 venus, 移植时改了个名称<br>
为避口舌特意选用了 virglrender 官仓中的最新版代码来移植<br>
(1.3.0, 没人移植过这个版本)<br>
未完善到可用的程度

| |virvk 目前的测试结果|
|--|:--|
|1|CPU内存中的素材无法上传到GPU<br>目前只能显示清屏、内绘矢量图等通过GPU接口绘制的画面|
|2|CPU-GPU间同步机制低效, 会拉低帧率|
|3|渲染加速接口可用 (vkmark 中的 clear 清屏测试项)|
|4|无需要修改 proot 中的 glibc mesa (25.2.8)|

| |virvk 测试设备|
|--|:--|
|1|红米-k40 , 安卓13, 骁龙 870(Adreno (TM) 650), 原厂vulkan驱动不支持dma-buf扩展也能用!|
|2|oppo-A93s, 安卓12, 天玑 700(Mali-G57 MC2)|

| |virvk 测试步骤|
|--|:--|
|启用zzwl|echo "droidvm-zzwl">$app_home/app_boot_config/gui_srv_libname.txt|
|启动软件管家|/exbin/tools/zzswmgr/zzswmgr.py<br>左侧的驱动分类, 安装 virvk, 然后重开app|
|启动vkmark|sudo apt install -y vkmark # 默认密码 droidvm<br>~/1|
|启动网页终端|zzwebterm, 非必须, 仅为方便测试|
