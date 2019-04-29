## Peer Paring problem（Antenna）
***
### Problem description

#### 测试工具
* 开发板： CDA DEVELOPMENT BOARD REV 2
* 核心板： QCC3020  CF223-1
* 程序配置工具： QCC3020_Earbud_Configuration_Kit_6.3.2.15
* 天线： 开发板默认出厂自带的SMA接头的天线,开发板默认的IPEX接口线
* CMD指令编译擦除烧录（**修改耳机左右LAP地址，修改XtalLoad、Xtal Freq**）
#### 测试步骤（**以下数据来自：超过十次的重新烧录以及配对**）
* 烧录好程序之后LED3快闪LED3  Red on 50(ms), Red off 50(ms) (repeat)，此时处于配对状态，当两块天线距离隔超过5-10CM时配对需要10-2min，10-20min后20%的概率可以配对上，其余的情况两块板子不能配对。

* 将两块板子的天线逐渐靠近在5cm范围甚至天线完全贴近的时候Peer Paring100%成功

#### 对比测试步骤（**以下数据来自：两次的靠近配对**）
* 和以上测试工具相比相比，本次测试改变量为：MDE编译工具2.3.0.115、ADK3.6.2
* 擦除Flash（为确保擦除成功：指令显示成功、拔出USB后开机指示灯无任何状态）
* 通过MDE编译和烧录（Bulid-All、Deploy--All。修改左右地址以及XtalLoad、Xtal Freq）
* 烧录完成后LED1蓝灯快闪 on 50(ms),  off 50(ms) (repeat)，配对状态
* 当两块板子天线逐渐靠近的时候（5CM以内配对100%成功）较远后很难配对成功

#### 结论
<font color=#f00>
* 确认开发板天线存在问题，后续需要测试天线的相关性能指标。
* 通过该测试需要向高通了解所有的EarBud配对需要达到什么样的天线性能方可在一米内（用户实际体验距离）轻易迅速的配对成功
</font>