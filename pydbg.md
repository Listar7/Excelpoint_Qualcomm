### pydbg
---
* 阅读文档ADK 6.x Pydbg Quick Start Guide User Guide

* 在windows的环境变量中添加ADk中安装的环境变量C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\tools\python27

* C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\apps\fw\tools>   //进入pydbg.py环境命令
#### usbdbg
* python pydbg.py -d tc:usb2tc -f app1:D:\Project\5121sink\apps\applications\sink\qcc512x_qcc302x\common\depend_Headset_qcc512x_qcc302x\sink.elf

* python pydbg.py -d tc:usb2tc -f audio0:D:\Project\5121sink\audio\kalimba_ROM_4786\kymera\output\stre_rom_v02_release\build\debugbin\kymera_stre_audio.elf

#### trbdbg（**建议使用**）
* python pydbg.py -d trb:usb2trb -f apps1:D:\Project\5121-avs\apps\applications\sink\qcc512x_qcc302x\common\depend_Headset_qcc512x_qcc302x\sink.elf

* python pydbg.py -d trb:usb2trb -f audio0:D:\Project\5121sink\audio\kalimba_ROM_4786\kymera\output\stre_rom_v02_release\build\debugbin\kymera_stre_audio.elf

* python pydbg.py -d trb:usb2trb -f apps1:D:\Project\5121-avs\apps\applications\sink\qcc512x_qcc302x\common\depend_Headset_qcc512x_qcc302x\sink.elf,audio0:D:\Project\5121sink\audio\kalimba_ROM_4786\kymera\output\stre_rom_v02_release\build\debugbin\kymera_stre_audio.elf