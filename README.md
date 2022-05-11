# SafeBTPanel

旧版本宝塔面板(去除弹窗)


## 安装(以centos为例)

### 1.使用官方脚本安装最新版本

```shell
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
```



### 2.使用旧版安装包升级

```shell
yum install wget -y
wget https://raw.githubusercontent.com/rroy233/SafeBTPanel/main/bt.zip
unzip bt.zip
rm -f bt.zip
cd panel && bash update.sh
```



### 3.去除弹窗

```shell
cd /www/server/panel/data/ && mv bind.pl bind.pl.1
```

### 4.屏蔽官方
```shell
echo "127.0.0.1 www.bt.cn" >> /etc/hosts
/etc/init.d/network restart
```
