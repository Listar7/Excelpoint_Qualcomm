# QCC3020_Earbud_Configuration_Kit_6.3.2.15

 ### 3020EarBud_Demo  Testing
 ---
 * LEDC闪硕两次然后关闭（2s）代表持续输出A2DP音频流
 * 同时开机配对基本可以在两秒内完成（包含每个耳机单独开关）
 * 蓝牙连接界面显示上排：昵称电量和aptX的Logo，下排：已连接|电量为66%|使用中
 * 当关闭连接耳机（Master）电源此时手机不会重连副耳机
 * 当主耳机插上5V--2A电源时（模拟用户充电插上USBC的时候）连接会动切换到副耳机但是播放音乐时音乐会自动暂停     
 * 当关闭副连接耳机，主耳机检测到副耳机断开后会有提示音：三声滴滴音效逐次降低（5s左右代表副耳机断开）重新连接时两声声音逐渐升高（2s）
 * 通话过程中（已连接情况下）反复切换听筒和蓝牙暂时没有问题

 * <font color=#f00>耳机**杂音**问题,存在某些耳机在播放音乐时候，当音调渐渐降低时候会出现杂音（电流杂音Maybe：耳机质量问题），开始播放音乐或者暂停音乐的时候都会有杂音存在,暂停的杂音会持续5s左右有时候会杂音一直存在。
 * 耳机在开关机的时候存在微量开机的杂音（Maybe：开发板开关机的时候电流不稳定）</font>

###  **Abnormal phenomenon**
 ---
* 当插拔USBC的时候或者开关VBAT的时候存在副耳机存在搜索不到的情况（测试此现象为偶发现象概率在5%左右）
* 在副耳机搜索不到的情况下灯两种闪烁状态（1.LED2亮1S然后熄灭2s。2.LED3持续闪烁（普通配对模式））
* 出现问题的地址及昵称：pskey_bdaddr={0x00ff01,0x5b,0x2},pskey_device_name="wllwjqBud_L"

* <font color=#f00>某次插上USBC或者开关VBAT的时候，偶发式的开机后两块板子工作异常现象LED3快闪。重新烧录程序后两块板子LD3快闪，无法配对（此现象在烧录后发生的概率非常大：90%），**放一段时间10-20min(两个Earbud配对成功)**后LD2闪烁复位其中一块板子可以搜索到wllwjQBud_L（左耳机），手机连接后wllwjqBud_R也可以被所搜到此时Earbud完全工作正常。</font>
* 存在一次耳机播放声音严重卡顿

### Testing day（2019-4-17）&Testing image**<font color=#f00>（8M&16M）</font>**
---
* 放一段时间第二天开机两个耳机运行正常，但是一次偶然开机（打开VBAT）之后又发现Left耳机出现Error的LED3快闪烁。Right耳机正常
* 多次将两个耳机都插上USB Charge（交替插拔两个USB重复二十次）问题依旧存在，Right依旧可以搜索到，Left搜索不到
* <font color=#f00>将两个Earbud开发板交叉烧录固件，重新烧录固件两个开发板(LED3)闪烁为Error的状态LED  On/Off(Repeat 100ms)，反复插拔USB-C(重复五十次)灯依旧为Error状态，此时两个开发板无法完成配对。</font>

**Note**经过十次的测试现象，发现其中一块开发板出现蓝牙昵称搜索不到的问题概率较大。
**<font color=#f00>以上配对不上的错误很可能是硬件问题，Maybe on Antenna，具体在哪里目前还需要进一步分析</font>**

### Earbud Completely works normal 
---
#### Play Music
*	Use the pair of earbud (A--Marster&B--Slave) as normal, play music.  Then plug in the USB-C cable (charging), the the earbud (e.g, A) should stop working while the B  can connect to the phone and working But Music will stop,in this situation one can short press Sys-Control to Play / Pause music. Then unplug the USB from A, the music can play on both. then plug USB-C to B, B will stop playing music,wihile unplug B it will immediately playing music.

#### Call situation
* 在通话过程中短按Sys-Control按键可以接听挂断电话，但是只有主耳机的MIC可以生效，副耳机MIC失效
* 当把**副耳机**插上USB-C的数据线的时候（Charge）副耳机将休眠，当拔出USB-C的时候声音恢复正常
* 当把**主耳机**插上USB-C的数据线的时候（Charge）手机依旧保持和主耳机的连接但是**副耳机**的Headphone和MIC都可以生效，当把主耳机的VBAT关闭的时候手机将会断开和主耳机的连接但是不会和副耳机自动连接（**Maybe：为了保持通话的连接所以在通话过程中不会在主耳机休眠的时候切换耳机打断通话的过程**）

### To build an Earbuds Application 
---
Before building the application, various filesystems on the device need to be updated depending on the hardware configuration and device specific settings.
1. Modify the Bluetooth Address:
a. Change the Bluetooth address in the **subsys1_config2.htf** file, which is located in the
<font                  color=#f00>\src\legacy\app\earbud\workspace\qcc3020_cdk\filesystems</font>
directory.
```

# Change bluetooth address and device name to appropriate values

#EB1
pskey_bdaddr={0x00ff00,0x5b,0x2}
pskey_device_name="wllwjqBud_R"

#EB2
#pskey_bdaddr={0x00ff01,0x5b,0x2}
#pskey_device_name="wllwjqBud_L"
```
2. Modify trims, by setting the correct xtal trims in the **subsys0_config3.htf** file, which is located in the
<font color=#f00>.\src\legacy\app\earbud\workspace\qcc3020_cdk\filesystems</font>
  directory.
```
  # Crystal trim.  Currently set to default values - modify as indicated by board
# label.

#EB1
#XtalLoadCapacitance = 11
#XtalFreqTrim = -4

#EB2
XtalLoadCapacitance = 11
XtalFreqTrim = 8
  ```
3. Modify application configuration settings as required in the **subsys7_psflash.htf** file, which is located in the
<font color=#f00> .\src\legacy\app\earbud\workspace\qcc3020_cdk\filesystems</font>
directory
### Flash Image
---
 ##### 进入安装目录，例如： D:\Software\earbud\QCC3020_Earbud_Configuration_Kit_6.3.2.15\tools>
 .\python27\python.exe create_image.py --config image_config_16M_dfu.ini    **（制作烧录镜像）**

 .\lib\bluesuite\NvsCmd.exe erase -usbdbg 101 -deviceid 4 0                    **（通过USBC擦除Flash）**

 .\lib\bluesuite\NvsCmd.exe burn .\output\flash_image.xuv -usbdbg 101 -deviceid 4 0   **（通过USBC烧录）**

 **Note：** 制作两个烧录镜像需更改地址为奇偶（左右耳机），XtalLoad以及XtalFreq需要改为对应的板子上实际标签值

**Advantage：** 以上三个步骤基本都可以在20s内完成，编译烧录效率远远大于Qualcomm--MDE

### Other Details
---
pelease check the Document： Qualcomm Earbuds Configuration Kit for QCC3020 User Guide
