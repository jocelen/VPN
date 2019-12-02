# CentOS6/7 专用破解版锐速一键安装

一、注意事项
1、安装锐速需降级系统内核，而安装 Google BBR 则需升级系统内核，故两者不能同时安装。
2、安装锐速需降级系统内核，有可能造成系统不稳定，故不建议将其应用在重要的生产环境中。
3、本教程只支持 CentOS6 x64 及 CentOS7 x64 系统，不支持任何 Debian & Ubuntu 系统！
二、判断系统类型
连接服务器，按照下图提示，我们首先复制命令：
`
uname -r 
`
然后回到 Xshell 软件，鼠标右键选择粘贴，回车继续。
￼
回车后输出当前系统内核版本。主要分三种情况：

1、结果以 2 开头，例如 2.6.32-696.18.7.el6.x86_64。
这种输出结果说明我们的服务器为 CentOS6 x64 系统，大家直接查看第三步进行锐速安装即可。

2、结果以 3 开头，例如 3.10.0-693.11.6.el7.x86_64。
这种输出结果说明我们的服务器为 CentOS7 x64 系统，大家直接查看第四步进行锐速安装即可。

3、结果以 4 开头，例如 4.12.10-1.el7.elrepo.x86_64。
这种输出结果说明我们的服务器已经安装 Google BBR 拥塞控制算法，此时已经无法继续安装锐速。

三、CentOS6 x64 系统安装锐速
若第二步中确定服务器为 CentOS6 x64 系统则看这一步。
按照下图提示，我们继续复制下列命令：
`
wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/jocelen/VPN/master/ServerSpeeder/appex.sh && bash appex.sh install '2.6.32-642.el6.x86_64'
`

然后回到 Xshell 软件，鼠标右键选择粘贴，回车继续。
￼
回车后系统会自动下载脚本并执行。按照下图提示，我们直接回车继续即可。
￼
回车继续后系统会自动安装锐速，同时会先后要求我们设置锐速的三项信息。按照下图提示，我们每次都直接回车继续即可。
￼
设置完三项信息完成后，系统会完成锐速安装并输出锐速的运行状态。按照下图提示，当出现红框内信息时说明锐速已完成安装并开机自启动。
￼
四、CentOS7 x64 系统安装锐速
若第二步中确定服务器为 CentOS7 x64 系统则看这一步。
按照下图提示，我们继续复制下列命令：
`
wget --no-check-certificate -O rskernel.sh https://raw.githubusercontent.com/jocelen/VPN/master/ServerSpeeder/rskernel.sh && bash rskernel.sh
`
然后回到 Xshell 软件，鼠标右键选择粘贴，回车继续。
￼
回车后系统会自动下载脚本并执行更换内核命令。按照下图提示，我们可以看到当前系统确实为 CentOS7，等待内核更换完毕后系统会自动重启并断开连接。
￼
系统重启后，Xshell 软件会断开连接。等待 3~5 分钟服务器即可重启完毕，我们重新连接服务器，按照下图提示，我们继续复制命令：
`
yum install net-tools -y && wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/jocelen/VPN/master/ServerSpeeder/appex.sh && bash appex.sh install
`
然后回到 Xshell 软件，鼠标右键选择粘贴，回车继续。
￼
回车后系统会自动下载脚本并执行。按照下图提示，我们直接回车继续即可。
￼
回车继续后系统会自动安装锐速，同时会先后要求我们设置锐速的三项信息。按照下图提示，我们每次都直接回车继续即可。
￼
设置完三项信息完成后，系统会完成锐速安装并输出锐速的运行状态。按照下图提示，当出现红框内信息时说明锐速已完成安装并开机自启动。
￼
安装教程就是这些，大家有不清楚的可以留言提问。
五.锐速常用命令
启动：/serverspeeder/bin/serverSpeeder.sh start
停止：/serverspeeder/bin/serverSpeeder.sh stop
状态：service serverSpeeder status
检查是否有appex0模块：lsmod
