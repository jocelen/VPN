# Vmess一键脚本使用方式


脚本适用于：Debian 9+ / Ubuntu 18.04+ / Centos7+

两个安装方式（不兼容，二选一）

1.Vmess+websocket+TLS+Nginx+Website
复制（或手动输入）下面命令到终端
`
bash <(curl -L -s https://raw.githubusercontent.com/jocelen/VPN/master/V2ray/vmess_ws_tls_bash-install_h2.sh) | tee v2ray_ins_h2.log
`
按回车键，将出现如下操作菜单。如果菜单没出现，CentOS系统请输入 `yum install -y curl`，Ubuntu/Debian系统请输入 `sudo apt install -y curl`，然后再次运行上面的命令：


证书报错 尝试
`yum install ca-certificates`

