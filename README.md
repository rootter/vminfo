##说明:
- 当前版本:1.6,更新日期:2015-11-24
- 在centos6.x平台上测试通过.
- 说明：列出当前宿主机上所有运行中的虚拟机(KVM)详细信息，注意此脚本只能列出运行状态的虚拟机

##更新日志
### 2015-11-24
1. 更新版本为1.6.
2. 使用"-i"参数可显示虚拟机ip地址.
3. 无法获取ip地址的虚拟机会用"-"代替.

### 2015-9-15
1. 更新版本为1.5
2. 可显示虚机每块磁盘大小.
3. 默认只列出虚机的根磁盘，加上"-d"参数可列出所有磁盘.
4. 使用"-v"参数可显示当前命令版本

##用法:
- 拷贝到/usr/local/bin/目录,并添加可执行权限，然后终端直接使用命令vminfo即可

##列解释：
- VHOSTS: 所有使用libvirt管理的运行中的虚拟机,关机状态下的虚拟机不会被列出.
- PID: 该虚拟机进程的PID,kvm虚拟机其实就是宿主机上一个标准的进程.
- %CPU: 该虚拟机进程所占用宿主机CPU百分比.
- %MEM: 该虚拟机进程所占用宿主机内存百分比.
- PORT: 该虚拟机console映射到宿主机上的vnc端口,可以通过宿主机的此端口连接到虚拟机console.
- Vcpus: 该台虚拟机vcpu个数.
- Vmems: 该台虚拟机虚拟内存大小.
- Vdisk: 该虚拟机所使用的虚拟磁盘(只列出该虚拟机系统盘).
