### docker 以特权模式运行容器，root可以执行systemctl系统命令
使用--privileged=true  /sur/sbin/init

docker run -d --name centos7-1 --privileged=true --network="bridge" --cpuset-cpus="0-8" -m 32768M centosnew:0.1 /usr/sbin/init ping 8.8.8.8
