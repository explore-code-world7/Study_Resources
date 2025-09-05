# capture-package

* tcpdump

```bash
sudo tcpdump -i   wlp3s0   src host 10.162.197.159 or src host 2408:8642:893:efca:c50a:d7fa:9861:bb12 -v -w netlog.pcp
```

* 用正则表达式

* 关闭upnp port

```bash
sudo  iptables -A OUTPUT -p tcp --dport 1900 -j DROP
sudo  iptables -A OUTPUT -p udp --dport 1900 -j DROP
```

* block connection to pycharm

```bash
sudo  iptables -A OUTPUT -p udp  -d  13.226.61.0/24 -j DROP
sudo  iptables -A OUTPUT -p tcp  -d  13.226.61.0/24 -j DROP
```

## wireshark

* 按时间过滤

```bash
frame.number<304&&
```

## example

- 发起到Amazon数据中心的连接

```bash
22:06:21.328814 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [S], seq 2039914549, win 64240, options [mss 1460,sackOK,TS val 4205879253 ecr 0,nop,wscale 7], length 0
22:06:21.639491 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [.], ack 2554775116, win 502, options [nop,nop,TS val 4205879564 ecr 2143088451], length 0
22:06:21.639895 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [P.], seq 0:284, ack 1, win 502, options [nop,nop,TS val 4205879564 ecr 2143088451], length 284
22:06:21.947492 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [.], ack 2746, win 544, options [nop,nop,TS val 4205879872 ecr 2143088762], length 0
22:06:21.947986 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [P.], seq 284:314, ack 2746, win 544, options [nop,nop,TS val 4205879872 ecr 2143088762], length 30
22:06:21.948048 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [F.], seq 314, ack 2746, win 544, options [nop,nop,TS val 4205879872 ecr 2143088762], length 0
22:06:22.254426 IP 10.162.55.89.48908 > 13.41.103.230.443: Flags [.], ack 2747, win 544, options [nop,nop,TS val 4205880179 ecr 2143089070], length 0
```

- 可用wireshark追踪数据流

- 靠，这是ubuntu系统更新的服务器

https://www.netify.ai/resources/ips/13.41.103.230

# app-authority

## firejail

```bash
sudo firejail --net=none  pycharm-community
```

```bash
Reading profile /etc/firejail/pycharm-community.profile
Reading profile /etc/firejail/allow-java.inc
Reading profile /etc/firejail/allow-common-devel.inc
Reading profile /etc/firejail/disable-common.inc
Reading profile /etc/firejail/disable-devel.inc
Reading profile /etc/firejail/disable-passwdmgr.inc
Reading profile /etc/firejail/disable-programs.inc
Warning: Warning: NVIDIA card detected, nogroups command disabled
Parent pid 9771, child pid 9772
The new log directory is /proc/9772/root/var/log
Blacklist violations are logged to syslog
Child process initialized in 86.12 ms
2025/06/03 09:15:37.344767 system_key.go:157: cannot determine cgroup version: cannot determine cgroup version: cannot statfs path: permission denied
^C
Parent received signal 2, shutting down the child process...

Child received signal 2, shutting down the sandbox...
```
