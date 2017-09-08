运行下面的命令获得MySQL admin用户的密码
```
sudo docker logs itopdocker_itop_1 | grep -C4 "mysql -uadmin -p"
```

MySQL root用户密码为空，只能localhost连接

运行下面命令安装itop虚拟机
```
vagrant up
```

按照 [itop安装指南](https://wiki.openitop.org/doku.php?id=2_4_0:install:install_wizard) 进行初始化配置

或者运行
```
php unattended_install.php default-params.xml
```

可以运行以下命令安装 [iTop Toolkit](https://wiki.openitop.org/doku.php?id=2_4_0:customization:datamodel#installing_the_toolkit)
```
sudo docker exec itopdocker_itop_1 /install-toolkit.sh
```

