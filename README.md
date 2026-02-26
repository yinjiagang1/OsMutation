# OsMutation
将任意 OpenVZ/LXC VPS 重装为 Debian/CentOS/Alpine

## 功能特性
- 支持 OpenVZ 7 和 LXC
- 支持重装为多种操作系统

## 使用方法
# 常规方式：
```
wget -qO OsMutation.sh https://raw.githubusercontent.com/LloydAsp/OsMutation/main/OsMutation.sh && chmod u+x OsMutation.sh && ./OsMutation.sh
```
或者
```
curl -so OsMutation.sh https://raw.githubusercontent.com/LloydAsp/OsMutation/main/OsMutation.sh && chmod u+x OsMutation.sh && ./OsMutation.sh
```
针对小硬盘 VPS（小于 1GiB，实验性支持）：

```
wget -qO OsMutation.sh https://raw.githubusercontent.com/LloydAsp/OsMutation/main/OsMutationTight.sh && chmod u+x OsMutation.sh && ./OsMutation.sh
```

[![asciicast](https://asciinema.org/a/582009.svg)](https://asciinema.org/a/582009)

## 注意事项 (Notice)
- 将会安装全新的系统，所有旧数据都会被清空！请务必先备份重要数据。
- 支持 OpenVZ 7 及以上版本，不支持 OpenVZ 6。
- 不支持 虚拟机（如 KVM、Xen 和 VMware）。

## 工作原理
OpenVZ 和 LXC 属于容器虚拟化技术，与宿主机共享内核。如果你想要替换操作系统，只需替换容器中的文件即可。就这样，简单明了。只需注意操作的顺序，因为文件之间存在一些依赖关系。

## 模板来源
LXC 模板下载自 linuxcontainers.org，OpenVZ 7 模板提取自官方 ISO。

## Thanks To
- Inspired by https://gist.github.com/trimsj/c1fefd650b5f49ceb8f3efc1b6a1404d

## To Do
- Support non-interactive mode by accepting arguments
- Support customed template source
- Support more operating system 
- Fix networking bug of CentOS under LXC
- Auto configure ipv6 network
