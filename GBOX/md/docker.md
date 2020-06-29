# 安装Docker环境

<table><tr><td bgcolor=#24256C><font face="黑体" color=#FADD0B size=4>

````bash
yum clean all; yum -y install epel-release; yum -y update
yum -y install bash-completion vim aria2 wget lrzsz iptables-services iftop iproute net-tools ntp mtr tcping openssl
curl -s https://download.docker.com/linux/centos/docker-ce.repo -o /etc/yum.repos.d/docker-ce.repo
yum -y install docker-ce    # CentOS 8 ~]# yum -y install docker-ce --nobest
systemctl enable docker; systemctl start docker
systemctl disable firewalld; systemctl stop firewalld
echo "ip_resolve=4" >>/etc/yum.conf
````

</font></td></tr></table>

    https://download.docker.com/linux/static/stable/x86_64/
    https://github.com/docker/compose/releases/