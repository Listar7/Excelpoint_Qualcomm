### 读取flash文件
---
* 以管理员权限运行CMD.exe
* 进入NvsCmd.exe的软件目录:C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\tools\bin>
* NvsCmd命令各个参数的详情：C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\tools\bin> NvsCmd -help
* 读取Flash中的固件:C:\qtil\ADK_QCC512X_QCC302X_WIN_6.3.2.24\tools\bin> nvscmd -trb 1 -deviceid 4 0 dump wllwj.XUV