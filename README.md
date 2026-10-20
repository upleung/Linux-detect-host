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


• 显示硬件及内核架构名称：

```
uname -m
```

	• 用途：直接输出硬件架构类型（如 x86_64、aarch64 等）。

  
• 查看详细的系统与内核信息：
```
uname -a
```

	• 用途：显示完整的内核版本、主机名、硬件架构及操作系统类型


• 查询服务
ps aux
free -v
df -h\



	1. 修复后的有效链接对照
完整版 Debian Bookworm (debian:bookworm)：

AMD64: [https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-amd64/bookworm/oci/blobs/rootfs.tar.gz](https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-amd64/bookworm/oci/blobs/rootfs.tar.gz)

ARM64: [https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-arm64v8/bookworm/oci/blobs/rootfs.tar.gz](https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-arm64v8/bookworm/oci/blobs/rootfs.tar.gz)

精简版 Debian Bookworm (debian:bookworm-slim)：

AMD64: [https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-amd64/bookworm/slim/oci/blobs/rootfs.tar.gz](https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-amd64/bookworm/slim/oci/blobs/rootfs.tar.gz)

ARM64: [https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-arm64v8/bookworm/slim/oci/blobs/rootfs.tar.gz](https://github.com/debuerreotype/docker-debian-artifacts/raw/dist-arm64v8/bookworm/slim/oci/blobs/rootfs.tar.gz)
