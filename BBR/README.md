# 优化加速

##  安装魔改bbr
* 可选参数: `-f v4.12.9 ` 内核版本号

```
wget --no-check-certificate -qO 'BBR_POWERED.sh' 'https://moeclub.org/attachment/LinuxShell/BBR_POWERED.sh' && chmod a+x BBR_POWERED.sh && bash BBR_POWERED.sh
```

输入 ` lsmod | grep 'bbr_powered' ` ,查看结果,不为空即为安装成功


## 检测

``` 
wget -qO- bench.sh | bash
```

