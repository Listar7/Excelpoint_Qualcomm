## Install MDk
---------------------

## Install ADk
## Install bluesuite.win.3.1.x （USB Driver）
Download&Instal:  BlueSuite.WIN.3.2 Installer
https://createpoint.qti.qualcomm.com/tools/#suite/6283/32201

以管理员权限运行CMD.exe程序，输入以下指令
find "USB\VID_0A02&PID_4010" *.inf > c:\inf.txt    将相关信息输出到inf.txt中

删除驱动
C:\Windows\System32>Pnputil -d -f oem7.inf或者Pnputil /delete-driver oem7.inf /force



在此目录下创建文件：C:\qtil\ADK_QCC512x_QCC302x_WIN_6.2.84\tools\bin      lock.txt并写入32个0 


然后在此目录下执行命令：TransportUnlock.exe writeunlockkey lock.txt


### 亚马逊AVS支持的开发板
---
Amazon AVS requires both the wake word and some noise for the wake word (pre-roll) to be
transferred to the Amazon Alexa app before the utterance. This requires the use of an SRAM
which is available on the following modules:
* QCC5127-AA/DEV BRD R2-AA

* QCC5126-AB/DEV BRD R2-AA 

###  Amazon  AVS  User_Guide
---
Install the ADK and Amazon AVS add-on software
**安装MDE、ADK、Amazon_AVS**
1. Run the standard ADK installer executable. For detailed instructions, see the QCC512x and
QCC302x/3x Development Kit and ADK 6.x Quick Start User Guide.
After the installation, a folder appears in the file system. For example,
C:\qtil\ADK_QCC512x_QCC302x_WIN_xxxxxx_ext_win_32.
2. Run the ADK Add-on for Amazon AVS installer executable
ADK_QCC512X_ROM_V21_WIN_Add_On_AmazonAvs_x.x.x.xx.
After installation, Amazon AVS can be configured, built, and deployed using the ADK
Configuration tool.


subsys7_config2
USBSerialNumberString = [ 41 42 43 44 45 46 30 31 32 33 34 35 36 37 38 39 ]

Enable Voice Assistant

DSP，CVC，ANC

### 按键配置
* 查看核板的管脚，然后将按键配置到相关的管教上面通过飞线以及使用ADk Configtool来实现。

* 编译出来的flash_image.xuv  按照8Mbit编译flash_image.xuv文件大小接近8MB字节

* 触摸按键，在开发板上进行调试



### EarBud通话测试
* 当在通话的时候,从耳机切换到手机听筒的时候副耳机不能挂断电话





### TWS Pluse（Earbud）
* 在Earbud工程里面找到av_headset_config.h里面屏蔽掉： #define DISABLE_TWS_PLUS
* 配对成功之后两个耳机会同时连接手机（仅支持高通845及以上平台）
* 在播放歌曲的时候可以任意无缝切换
* 接听电话时任意一个都可以接听和挂断
* 通话的时候**将手机切换为听筒模式两个耳机都可以挂断电话**
* 测试sink（3026-adk6.3.2）、TWS+（3020-adk6.3.2）双击sys-control不能直接挂断电话(可以通过ADK cotrol tool配置)

### Basic knowledge
---
### 耳机
* 支持快充
* 听力EQ曲线
* Alexa的Wi-Fi扬声器(Marshall) 
* 降噪（ENC环境降噪）
* ANC、ENC、CVC、DSP降噪
* 主动降噪根据拾音麦克风位置的不同，分为前馈式主动降噪与反馈式主动降噪
* https://zhuanlan.zhihu.com/p/61208255

### 动圈动铁
* 动圈单元：最常见、最传统的发声单元，薄膜上附有导线圈，利用电流流过导线圈产生磁场，磁场和永磁材料相互作用，推动薄膜振动产生声音
* 动铁单元：音圈是缠绕在位于永磁场中央的平衡衔铁上，这块衔铁通过磁力的作用带动发声


### 触摸式按键
* 单击播放暂停、接听电话挂断电话
* 双击上一曲下一曲、拒接电话
* 滑动调音
* 长按2S唤醒语音助手、或者唤醒词唤醒。单独的按键单击呼出语音助手
* 手机app自定义按键功能

### appliciation
* 无线耳机
* 无线音频市场的原始设备，蓝牙耳机现在是手机的必备配件。新的高性能解决方案允许您在办公室或旅途中拨打和接听电话，同时还提供高级音乐体验选项。

* 无线扬声器
* 无论是家中的高保真娱乐系统还是海滩或公园的便携式选择，都有一个可以想象的形状和大小的扬声器，以满足您的特定需求。即使这恰好在游泳池中。

* 车载系统
* 作为汽车市场的中流砥柱，蓝牙技术在今天销售的新车中占90％以上。蓝牙无线接入可以提高驾驶员的安全性并增强车内娱乐体验。

### pydbg
* PS C:\WINDOWS\system32> [Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\tools\python27")

* 在windows的环境变量中添加ADk中安装的环境变量

* C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\apps\fw\tools>   //进入pydbg.py环境命令

* python pydbg.py -d tc:usb2tc -f app1:D:\Project\5121sink\apps\applications\sink\qcc512x_qcc302x\common\depend_Headset_qcc512x_qcc302x\sink.elf

* python pydbg.py -d tc:usb2tc -f audio0:D:\Project\5121sink\audio\kalimba_ROM_4786\kymera\output\stre_rom_v02_release\build\debugbin\kymera_stre_audio.elf




