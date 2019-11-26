# Vmess一键脚本使用方式


脚本适用于：Debian 9+ / Ubuntu 18.04+ / Centos7+

两个安装方式（不兼容，二选一）

1.Vmess+websocket+TLS+Nginx+Website
`
bash <(curl -L -s https://raw.githubusercontent.com/jocelen/VPN/master/V2ray/vmess_ws_tls_bash-install_h1.sh) | tee v2ray_ins.log
`


2.Vmess + HTTP2 over TLS
`
bash <(curl -L -s https://raw.githubusercontent.com/jocelen/VPN/master/V2ray/vmess_ws_tls_bash-install_h2.sh) | tee v2ray_ins_h2.log
`


脚本启动方式

启动 V2ray：systemctl start v2ray

停止 V2ray：systemctl stop v2ray

启动 Nginx：systemctl start nginx

停止 Nginx：systemctl stop nginx

脚本相关目录

Web 目录：/home/wwwroot/levis

V2ray 服务端配置：/etc/v2ray/config.json

V2ray 客户端配置: 执行安装时所在目录下的 v2ray_info.txt

Nginx 目录： /etc/nginx

证书目录: /data/v2ray.key 和 /data/v2ray.crt
