## 引导背景知识：

Legacy和UEFI指的是系统引导方式(Legacy为传统BIOS，UEFI为新式BIOS)，MBR和GPT指的是磁盘分区表类型。

一般情况下都是Legacy+MBR， UEFI+GPT这两种组合。但Legacy+GPT，UEFI+MBR也可以实现



# win10+ubuntu 双系统安装：

win10 引导linux实现。

工具：

1. Ubuntu 20.04 ISO 镜像。
2. Etcher 软件或rufus.exe（用于制作一个可引导 Ubuntu 的 USB 驱动器）
3. 载启动项编辑工具EasyBCD（配置win10引导linux）



注意事项：

已刘工台式机为参考：

他的台式机：3块硬盘：1块当前系统是Legacy+MBR ，另一块是UEFI+GPT，还是一块固态。



**ubuntu安装在UEFI+GPT分区下，然后想让第一块win10 Legacy引导UEFI，必须在安装时不能创建efi系统格式，忽略警告。然后引导用/boot来。**



**还用用easybcd配置linux引导一定选grup2来引导。**





参考链接：

https://www.cnblogs.com/masbay/p/10745170.html

