### VMware上安装的centos7使用ping报错：name or service not known
#### 一、需要把虚拟机的网络连接设置为“NAT模式”
![NAT](images/网络适配器使用NAT模式.png)

#### 二、获取网络信息
![network_message](images/网络信息.png)
![network_message2](images/网络信息2.png)

#### 三、编辑IP，子网掩码，网关等信息
```
vi /etc/sysconfig/network-scripts/ifcfg-ens33
```

![network_config](images/配置网络信息.png)

#### 四、查看ip
```
ip addr
```

![network_address](images/查看ip地址.png)

#### 五、重启网络
```
service network restart
```

#### 六、最后测试网络连接
```
ping www.baidu.com
```

![network_test](images/测试网络连接.png)
