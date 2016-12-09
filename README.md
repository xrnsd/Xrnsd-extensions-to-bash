#android mmi开发环境的bash简单扩展
![Logo](data/logo.png)
##1.工程结构
####Xrnsd-extensions-to-bash在下面简写为xbash
	cmds/config	---------------------	工具相关配置
		config/bashrc_root_work_lz		为root相关bash配置文件
		config/bashrc_base				为普通用户相关bash配置文件
		config/bashrc_work_lz			为作者使用的普通用户相关bash配置文件
		config/bashrc_home				为作者在家使用的普通用户相关bash配置文件
		config/init_system.config		android build环境初始化工具的配置文件

	cmds/data	---------------------	工具相关数据
		data/excludeDirsAll.list		备份排除[忽略]全部列表
		data/excludeDirsBase.list		备份排除[忽略]基础列表
		data/user-dirs.dirs				home下默认文件夹配置
		data/value						全局参数

	cmds/module	---------------------	脚本实现文件[具体功能]
		module/system_backup_restore.sh	xbash的系统维护
		module/test.sh					xbash的demo测试,请忽略此文件的修改
		module/tools.sh					xbash的函数实现
		module/pytools					xbash的脚本测试工具
		module/compile.sh				xbash的项目编译初始化
		module/init_xbash.sh			xbash环境初始化工具
		module/init_system.sh			android build环境初始化工具

	cmds/main.sh	-------------------	xbash主入口

##2.初始化环境

	cd Xrnsd-extensions-to-bash
	./module/init_xbah.sh

##3.其他
	1 已验证环境
		ubuntu12.04 x64
		ubuntu14.04 x64
		ubuntu16.04 x64

	2 环境目录
		/home/xxx/tools	-------------------	环境相关工具
			tools/sdk
			tools/ndk
			tools/jdk
			tools/eclipse
			tools/sp_flash_tool
			tools/xls2values
		/home/xxx/cmds	-------------------	本项目目录
		/home/xxx/.bashrc	---------------	普通用户bash配置
		/root/.bashrc	------------------	root用户bash配置

	3 xc ,xb 为命令分类，搭配参数时和其余命令一样指向具体功能实现
	4 对记录和校验版本包软件和硬件信息相关实现修改，会影响历史备份的使用[导致检测失败]
	5 xx[休眠]建议不要开启，这玩意脾气不好
	6 提示找不到命令
		打开终端
		sudo chmod 777 -R /home/xxxx/cmds
