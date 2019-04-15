DOSBox-MASM环境的配置
===

下载工具
---
- [下载dosbox程序](https://www.dosbox.com)
- [下载masm全套汇编工具](https://pan.baidu.com/s/1afyrOoK6grfdl6v1W4nsNg) |提取码: a9y9|


masm文件夹
---
- masm.exe：汇编程序，用于汇编源程序(.asm)，得到目标程序(.obj)；
- link.exe：连接程序，用于连接目标程序，得到可执行程序(.exe)；
- debug.exe：调试程序，用于调试可执行程序。
- exe2bin.exe：将汇编生成的EXE文件转换成bin文件

安装配置(macOS为例)
- 安装dosbox程序
- 在**用户目录**建立一个文件夹例如DOSBox，将masm文件夹放入其中
- 在**DOSBox**建立一个文件夹例如asm，用于存放汇编程序
- 将dos挂载到dosbox的驱动器下
   + 例如挂载到dosbox的c驱动器下
   + 运行dosbox，键入`mount C /Users/user_name/DOSBox` (user_name为实际用户名)
- 省去手动挂载
   + macOs中的dosbox配置文件在`~/Library/Preferences/DOSBox\ 0.74-2\ Preferences`
   + 键入`vim ~/Library/Preferences/DOSBox\ 0.74-2\ Preferences`
   + 找到`[autoexec]`添加四行
      - 挂载驱动`mount C /Users/user_name/DOSBox`
      - 切换驱动`C:`
      - 添加环境`path=C:\masm`
      - 进入程序编写目录`cd \asm`