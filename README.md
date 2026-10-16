# Linux-detect-host
一键检测 Linux 宿主机配置脚本，查询容器宿主机硬件配置

### 查询配置： 

```
curl -sL https://raw.github.com/tdulcet/Linux-System-Information/master/info.sh | bash -s

```

### 查询IPV4 IPV6:

```
curl -4 ip.sb
curl -6 ip.sb

```

### 查询开放的端口（查看所有监听端口（TCP + UDP））

```
sudo ss -tulnp

```

### 查询外部服务器通信端口：

```
netstat -an | grep "ESTABLISHED" | egrep -v "127.0.0.1|::" | awk '{print $5}' | sort -u | sed -e 's/:/ /'

```
