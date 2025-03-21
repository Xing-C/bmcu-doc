# 版本

::: warning 注意
该内容由很强的时效性，请留意页面最低端的`最后更新时间`，若太久没更新可以找群友问，亦可提醒`@丸子`更新
:::

::: tip
下文中提到的`官方版`是指由BMCU开发组制作的版本
:::

## 整体版本

大致分为`130电机版`和`370电机版`

另有:

- 群友`@白小淘`制作的`180电机版`
- 群友`@星尘`进行更多改动的`BMCU370x`贴片微动版
- 欢迎改版作者联系`@丸子`，加入wiki

主板通用，但固件、外壳、部分机械零件有所区分、需确定一个版本并进行了解差异

::: info 提示
370是主动送料，一直送料到缓冲顶起，缓冲灯不亮就停止送料；
130是被动送料，料管耗材减少压缩缓冲，缓冲灯一亮就送料
@゛少年谈情不说爱℡
:::

### 130电机版

> 该版本固件需使用`0.2`版本

该版本是早期版本，其维护点主要在于`三角板离合`结构，特别适用于A1系列打印机，能够提供良好的稳定性，但结构较为复杂，三角板不够可靠等问题仍然存在

::: info 提示
该版本设计采用的`万宝至FF130-SH`电机目前貌似仅能通过闲鱼购买，详细信息查看[材料清单](./list.md)的说明
:::

该版本资料位于群文件`/bmcu整合包`中，本站包含该版本装机教程，还有视频教程可以[前往哔哩哔哩](https://www.bilibili.com/video/BV1PuPCehEP3)观看

#### 180电机版

该版本由群友`@白小淘`制作，属于特殊的`130电机版`，旨在解决130电机不易购买的问题，固件与结构和130版一致

#### 130钢珠版

由群友制作，目前资料少

### 370电机版

>该版本可以尝试使用`2-6` `3-14`等等版本的固件

该版本目前**正在开发和改进**，后续会进行设计修改

::: warning
目前缺陷：由于结构为直驱主动送料导致的爆五通，可以通过关闭切料时回抽、使用缓冲加长版、外置缓冲、五通增稳打印件等方式缓解
:::

该版本结构简单，电机易于购买，但由于尚未结束设计，资料较少，改版繁杂，该电机是P1系列打印机的前提，因130电机稳定且缓慢，会导致送料失败。

该版本同样适用于A1系列，以及P/X系列 `@星尘 ：觉得更适用于P1系列`。

该版本资料位于群文件`/370电机资料`文件夹

该版本有多个分支版本：

#### 370微动版（星尘改版）

该版本使用微动开关替换了耗材检测，避免了耗材光电孔容易被碎屑堵塞的问题，但主板也需要使用对应改版

#### 370钢珠版（）

该版本使用钢珠+弹簧来顶起上面的挡片遮挡光电开关，规避了耗材碎屑进入耗材孔的问题，主板和原版一致

## 外壳版本

::: warning 注意
外壳版本鱼龙混杂，版本繁多，可以跟着教程做，使用教程中使用的版本
:::

## PCB版本


### 原版（官方）

该版本就是最普通的版本，不多赘述

[开源链接](https://oshwhub.com/bamboo-shoot-xmcu-pcb-team/bmcu)

### C口版本（官方）

该版本添加了板载USB转TTL的CH340芯片，烧录的时候无需外置转换模块，除此之外和普通版没什么区别

[开源链接](https://oshwhub.com/bilibili233/bmcu0000)

### BMCU370x星尘改版

这是[星尘微动修改版](../build/bmcu370x.md)使用的主板

该版本板载USB转TTL的CH340芯片，烧录的时候无需外置转换模块，拥有二极管保护单片机。

改变了耗材检测部分，在光电的基础上可选微动来进行检测。

增加了一路DCDC降压，默认可通过焊盘切换使用的电机，12V和24V。

该版本仍然保持兼容原版

更多信息请看开源链接。

[开源链接](https://oshwhub.com/xingcc1/bmcu-370x)

### 霍尔缓冲版（官方）

这是开发组目前正在测试的最新主板，相比前一代主板目前主要新增了486浮地保护（采用pmos）、霍尔缓冲器（由上一代的数字值缓冲改为模拟值缓冲），该版本暂未稳定，敬请期待
