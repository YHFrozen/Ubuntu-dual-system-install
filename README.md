## Ubuntu系统安装
### 安装方式
本人采用的是双系统模式下的ubuntu安装，由于安装的时间早于教程发出的时间，(由于当时不太清楚软件最好不要装新的) 所以安装的是24.0.04版本，全程基本上是按照B站上的[Windows和Ubuntu双系统的安装与卸载](https://www.bilibili.com/video/BV1554y1n7zv/?share_source=copy_web&vd_source=019d9839ba6504b3270f63a06469b227 "视频链接")来进行的。
最开始本人曾把Ubuntu装到了移动机械硬盘上，后来发现硬盘读写速度只有70MiB/s，实在是太慢了，所以最后装到了笔记本上面。笔记本型号是Lenovo-XiaoXinAir-14ITL-2021。

### 下载镜像软件
在 cn.ubuntu.com/download 中下载官方的ubuntu镜像文件（但本人在制作完安装盘之后为了腾出更大的空间装系统所以把镜像文件给删除了:confounded::confounded::confounded:）


### 制作安装盘

不同于教程，本人选择rufus为镜像工具，选择以iso镜像文件写入，随后等待安装盘制作完毕。

### 磁盘分区

本人有140G左右的自由支配空间，选择分配方案如下：

|分区|容量大小|
|:--:|:--:|
|/efi|1Gib|
|/|138Gib|

本人没有配置 **/swap** (感觉不太需要)与 **/home** (感觉本来空间就不大所以就没想再分)

为了避免之后格式化的时候把自己的数据都清除掉，本人决定每隔一段时间就把数据导入自己的硬盘中备份一次(感觉这样和/home也差不了多少了)

### 使用安装盘安装

重启电脑，然后狂按**F12**键，进入笔记本的**BIOS**界面，选择Ubuntu，然后跟随引导安装（感觉这个部分也没有什么要说的，选择自定义安装，跟随引导一步步进行就好了）。
当然由于版本不太同的原因，ubuntu24的分区部分和之前旧版本有所不同，本人分区如下（同之前[方案](#磁盘分区)）：
|分区|分区类型|挂载点|
|:--:|:--:|:--:|
|EFI分区|VFAT|/boot/efi|
|Root分区|Ext4|/|

### 打开Ubuntu系统

重启电脑，拔掉安装盘，新建用户，就可以开始使用ubuntu系统。至此安装完毕。