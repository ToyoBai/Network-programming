1.查看端口号占用情况

	1.1 lsof		打印所有占用端口列表curl ifconfig.me
	1.2 lsof | less		分页显示
	1.3 lsof -i:port	查看某个端口是否被占用 (如果端口被占用，则会返回相关信息，如果没被占用，则不返回任何信息)

2.关闭占用端口

	2.1 kill PID		根据1.3获得PID，杀死相关进程
	
3.查看本机公用ip

	3.1 curl ifconfig.me	打印本机公用(外网)ip	
