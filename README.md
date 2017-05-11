# rocketmq-completion

rocketmq-completion是为[rocketmq](https://github.com/alibaba/RocketMQ)开发的命令行自动补全工具，借助Linux的[complete](http://info2html.sourceforge.net/cgi-bin/info2html-demo/info2html?%28bash.info.gz%29Programmable%2520Completion)技术实现，方便用户使用rocketmq时，减少命令行交互的成本及出错的概率。

## 安装
#### [推荐]标准安装方式

* 确保本用户Home目录下存在`.bash_completion`文件和`.bash_completion.d`目录
* 在`.bash_completion`文件中增加如下内容

```bash
for bcfile in ~/.bash_completion.d/* ; do
  . $bcfile
done
```
* 从[releases](https://github.com/jerrysearch/rocketmq-completion/releases)下载`mqadmin_completion`文件到`.bash_completion.d`
* 重新登陆当前用户或执行`source mqadmin_completion`
* 检查脚本是否生效

```bash
complete -p | grep -e mqadmin
```
输出中出现如下内容表示成功

```bash
complete -F _mqadmin mqadmin
```
#### 通用安装方式

* 从[releases](https://github.com/jerrysearch/rocketmq-completion/releases)下载`mqadmin_completion`文件到本地
* 在`~/.bash_profile`中增加如下命令

```bash
source /path/mqadmin_completion
```
* 重新登陆当前用户或执行`source ~/.bash_profile`
* 检查脚本是否生效

```bash
complete -p | grep -e mqadmin
```
输出中出现如下内容表示成功

```bash
complete -F _mqadmin mqadmin
```
## 用法

```bash
./mqadmin [tab]
./mqadmin [-tab][--tab]
```

**-表示必选参数，--表示可选参数**
				
## 关于升级
* 目前只实现了mqadmin脚本的自动补全，若增加对新命令的支持，使用方式同上
* 对单个脚本的更新，下载新版脚本并覆盖老版本即可

## 关于作者

爱Coding的程序员一枚


