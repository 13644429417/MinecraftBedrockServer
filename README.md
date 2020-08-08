# Minecraft Bedrock Server
本仓库必须克隆，在目录内运行./SetupMinecraft.sh<br>
因为目前我的世界基岩版服务器官方下载链接是国外的，所以还是比较慢<br>
本仓库部署命令：
<b>部署命令</b><br>
sudo apt-get update&&sudo apt-get install git -y&&git clone https://gitee.com/xingguangk/MinecraftBedrockServer.git&&sudo chmod -R 777 MinecraftBedrockServer&&cd MinecraftBedrockServer&&sudo chmod +x SetupMinecraft.sh&&./SetupMinecraft.sh<br>
<br>

############################################################################################################################################################################################################################################################

在Ubuntu/Debian/Raspbian/Armbian上设置Minecraft基岩专用服务器，提供自动更新、备份和启动时自动运行的选项<br>
查看安装说明：https://jamesachambers.com/minecraft-bedrock-edition-ubuntu-dedicated-server-guide/<br>
<br>
<b>测试分布</b><br>
-Ubuntu / Ubuntu Server 18.04.2<br>
-Debian Stretch / Buster<br>
<br>
<b>测试平台</b><br>
-PC X86_64<br>
-Udoo X86<br>
-Intel Compute Stick<br>
-ARM 64bit (warning: proof of concept, extremely slow)<br>
--Raspberry Pi<br>
--Tinkerboard<br>
<br>
<b>更新历史记录</b><br>
<br>
2019年7月24日<br>
-固定树莓派支持<br>
<br>
2019年7月10日<br>
-修正了1.12中的OpenSSL错误（感谢obviator！）<br>
-固定端口不选择默认值，如果没有输入（谢谢sweavo！）<br>
<br>
2019年7月2日<br>
-在安装程序脚本中添加了libcurl4基岩服务器依赖项，以防止服务器启动失败<br>
<br>
2019年7月1日<br>
-增加了对多个服务器的支持<br>
-在中选择服务器的文件夹名称和端口SetupMinecraft.sh（每个服务器实例必须唯一）<br>
<br>
2019年5月23日<br>
-修正了输入错误重新启动.sh其中有一个空格后停止命令阻止服务器干净地关闭<br>
-在强制关闭后增加了10秒的睡眠时间，以便在调用之前让服务器有时间完全关闭开始.sh<br>
-修复了服务器在计划的夜间重新启动后未重新启动（与重新启动.sh错误）<br>
-删除了一些损害跨平台兼容性的直接（例如/bin/sleep）路径<br>
<br>
2019年4月26日<br>
-测试了新的基岩专用服务器1.11.1.2<br>
-在服务器上增加了启动计数器，而不是等待一个平坦的4s，以减少不必要的等待<br>
-固定臂支架（需要64位）<br>
<br>
2019年4月18日<br>
-将StopChecks++更改为StopChecks=$（（StopChecks+1））以提高可移植性（谢谢Jason B.）<br>
-在服务器上添加了timeoutpartsec=600，以防下载服务器的时间比平时长<br>
<br>
2019年3月7日<br>
-增加了Armbian支持<br>
-使用Tinkboard进行测试<br>
-修复了route vs/sbin/route的可移植性问题<br>
<br>
2019年3月2日<br>
-运行SetupMinecraft.sh脚本安装后，现在更新所有脚本并重新配置minecraftbe服务<br>
-脚本现在可用于任何基于Debian的发行版（Ubuntu、Debian、Raspbian等）<br>
-增加了对ARM平台（如Raspberry Pi）的*非常慢*的支持，QEMU仿真x86帴64<br>
-将服务重命名为minecraftbe，以避免与Java版本混淆<br>
<br>
2019年2月15日<br>
-备份现在压缩到。焦油gz格式（保存在备份文件夹中）<br>
-启动服务等待internet连接最多20秒，以便DHCP有时间检索IP地址<br>
-删除了不必要的睡眠时间停止.sh编写脚本，以便在minecraft服务器关闭时立即返回<br>
<br>
2019年2月8日<br>
-初始版本<br>

原仓库：https://github.com/TheRemote/MinecraftBedrockServer<br>