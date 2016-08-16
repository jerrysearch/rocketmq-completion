# rocketmq-completion
## 介绍

[rocketmq-completion](https://github.com/jerrysearch/rocketmq-completion)是为[rocketmq](https://github.com/alibaba/RocketMQ)开发的命令行自动补全工具，主要方便用户使用rocketmq时，减少命令行交互的成本及出错的概率!

## 安装

rocketmq-completion只有一个脚本，借助Linux中complete及compgen技术实现

* 从github上download到本地或服务器任何目录下，例如：/your_path/rocketmq-completion/rocketmq_completion
* 在本机bash_completion.d目录下，建立对应软连接(需要root权限)，注：不同Linux发行版目录地址不同，用户可根据自己系统版本 google


		cd /etc/bash_completion.d/
		ln -s /your_path/rocketmq-completion/rocketmq_completion

* 在bash_profile下填加一行
	
		source /etc/bash_completion.d/rocketmq_completion

* 重新打开一个新窗口，检查completion是否起作用

		complete －p
		
		
* 输出中出现以下内容表示成功

		complete -F _mqadmin mqadmin
		
## 用法
	./mqadmin[tab]
	./mqadmin clusterList [-tab][--tab]

参数部分 -表示必选参数，--表示可选参数
		
		
		
## 关于升级
* 目前版本只实现了mqadmin脚本的自动补全
* 未来对其它脚本的补全会持续更新，实现方式是在rocketmq_completion脚本下添加\_command方法并complete -F  \_command command方式来实现，以上用法中的步骤用户无需重复操作，即可实现对新增命令的支持

## 关于作者
自封首席程序员，哈哈
