# DELL7472 Clover、OC配置文件及驱动（也可供7572机型参考，二者主要存在屏幕大小的区别）

自20191017起：
Clover的配置文件已经非常稳定，之后不会再有大幅度的更新，目前已经全面切换到OC，今后会在OC上面持续更新。

特别注意：安装使用黑苹果之前，需要在BIOS里面进行如下设置，3项设置缺一不可，都是必须要设置的，否则将会导致引导出现问题：

1.关闭『安全引导』

2.开启AHCI

3.关闭『Enable Legacy Option ROMs』

目前完全支持10.15且兼容10.14、10.13等系统，功能及驱动等等一切正常。

具体文件请到发行页面下载：https://github.com/ic005k/DELL7472/releases



机器配置如下：

BIOS版本：1.3.1（目前最新的，建议大家及时更新BIOS）

CPU：i5-8250U

声卡：ALC256（目前音频ID采用56）

内存：8G

核显：UHD620

独显：无（同时显卡的设备属性里面已添加屏蔽独显的代码）

硬盘：256G SSD

无线网卡：BCM94360CS2（后来更换，免驱）



特别注意：

1.我使用的是苹果原装网卡BCM94360CS2，所以驱动里面没有放任何无线网卡和蓝牙的驱动程序，大家自行根据自己的无线网卡型号放入相应的驱动。

2.声卡耳机、耳麦需要单独驱动，否则耳机不响。驱动文件在kext目录里面，里面有安装说明和注意事项。耳麦驱动源自：https://github.com/hackintosh-stuff/ComboJack

个人目前建议不要驱动耳麦，驱动耳机就可以了。否则每次睡眠唤醒之后都会有一个对话框弹出来，让你选择耳机或者耳麦，比较扰人，呵呵。

目前存在的问题：

1.如果在插上耳机的情况下进入Recovery，此时选择『重启系统』，会导致机器直接关机。需拔下耳机并关掉交流电源，等待5分钟左右，才可以正常开机。目前此问题无解。
所以，如果进行OTA升级或安装新系统，建议拔掉耳机再进行。

2.如果使用VirtualSMC，在睡眠唤醒的情况下，有一定的机率出现唤醒后耳机无声。FakeSMC不存在这个现象。

最后对所有的贡献者和参与者一并表示感谢！
