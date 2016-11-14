


#文件及文件夹创建删除
	mkdir  文件名称	(创建文件夹)
	touch  文件名称	(创建文件)
	rm -r  文件名称 	(递归删除)
	rm -rf 文件名称   (删除文件夹内的所有 无提示)
	rmdir 文件名称    (删除文件夹)


#查看.搜索.历史
	ls -a 查看所有	(包括隐藏目录)
	ls -l 查看		(以列表的形式显示)
	head a -行数 文件名称  	(查看文件前多少行)
	history  				(查看历史操作命令)
	ls | grep s		(| 管道符 用于传递参数   将ls的查询结果 作为参数传递给 grep 查找其中包含s的内容)

#复制.写入
	ls >index.html			(重定向:改变默认 重定向另一位置)
	echo 内容>要写入的文件 	(覆盖原有内容)
	echo 内容>>要写入的文件 	(追加内容)
	mv a.text 目录/新名称  	(移动)
	cp a.text 目录/新名称  	(复制)

#请求	
	wget 网址              (下载文件)
	curl http://www.baidu.com   (发送请求)
	curl http://www.baidu.com > 要写入的文件
	whoami				(查看当前用户)

#vi模式
	##底行模式
		set nu 			(设置行号)
		wq				(退出保存)
		q!				(退出不保存)
		/要搜索的内容  	(在vi模式下 n为下一个目标元素 )
		e! 				(撤销更改，返回到上一次保存的状态)
		
	##命令模式
		-u 				(撤销操作)
		yy 复制  p粘贴
		G				(光标移动到最下面)
		gg				(光标移动到最上面)
		dd				(删除行)
		i				(编辑模式 可写入内容)
		ZZ				(大写 保存并退出)
		u				(辙销操作，可多次使用)
		ctrl+f			(向前翻页)
		ctrl+b			(向后翻页)

#版本控制
	svn(集中式) : 缺点
		1 由于是集中式版本控制系统所以严重依赖与服务器
		2 严重依赖网络 
	Git(分布式)
		1 不需要中央服务器 每个人一个完整的版本库
		2 版本库来自本地 不受网络限制


#git的使用
	1 git init  	(初始化仓库 或将以后的克隆到本地.giy/)
	2 git add -A	(放入暂存区有三种方法   路径/名称   -A  * )
	
	3 git commit -m'备注信息'  				(从暂存区放入仓库)
	4 git config --global user.email 邮箱  	(config只需要配置一次)
	  git config --global user.name  用户名
	
	5 git log 				(查看当前版本 以及历史存盘点)
	6 git status 			(查看当前厂库状态 那些被修改了)
	
	7 git checkout 文件名 			(暂存区还原原到工作区)
	8 git reset --hard 提交的id 		(每次提交时候都会生成一个id标示 git log可以查看)

