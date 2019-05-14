### amazon-avs
--- 
#### 版本：ADK_QCC512x_add-on_for_Amazon_AVS.WIN.6.3.2 Installer、ADK_QCC512x.WIN.6.3.2 Installer	Audio Development Kit (ADK) to support the QCC512x Bluetooth Audio Flash Platform	6.3.2.36
#### 使用硬件Qcc5121

* 仔细按照80-cg742-1_ae_adk_add-on_installer_for_amazon_avs.pdf文档步骤操作
* 在使用ADk configtool的时候设置该项的时候VA Press to Talk Start short，其它三项可以不用设置。
* 拔掉手机sim卡,重启手机
* 手机语言设置为英语（如果设置为中文启动App的时候会显示超时）
* 确保手机VPN可以访问外网
* 下载Fake Gps把地址设置为美国某个地区，手机打开开发者模式需要在手机里设置允许第三方软件模拟GPS位置
* 下载并注册Amazon Alexa账号
* 手机连接释放的蓝牙信号
* 打开app并在app中添加headphone设备此时会显示设备点击连接即可
* 连接成功后通过配置的按键按下触发语音助手即可语音交互（高通开发板的默认麦克风是MIC1）

##### error：如果Amazon alexa登陆后最下面只有三个导航栏则请sign out 后重新按照上面配置手机的步骤配置手机，正常的界面是app最下方有五个导航栏，在最右边的Device出添加自己的设备