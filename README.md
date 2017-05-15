# Rocketmq Completion

[![GitHub release](https://img.shields.io/badge/release-download-orange.svg)](https://github.com/jerrysearch/rocketmq-completion/releases)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

**[RocketMq Completion]() is a tool, support bash tab completion for [Apache RocketMq](https://github.com/apache/incubator-rocketmq) bash command**

Use [complete](http://info2html.sourceforge.net/cgi-bin/info2html-demo/info2html?%28bash.info.gz%29Programmable%2520Completion) technology to reduce the cost of command-line interaction and the probability of error

## install
#### [Recommend] Standard installation method

* Make sure that the `.bash_completion` file and` .bash_completion.d` directory exist in this user's home directory
* Add the following to the .bash_completion file

```bash
for bcfile in ~/.bash_completion.d/* ; do
  . $bcfile
done
```

* Download `mqadmin_completion` file from the [releases](https://github.com/jerrysearch/rocketmq-completion/releases) to `.bash_completion.d`
* Log in to the current user or execute `source mqadmin_completion`
* Check that the script is valid

```bash
complete -p | grep -e mqadmin
```
The following appears in the output as successful

```bash
complete -F _mqadmin mqadmin
```
#### Universal installation method

* Download `mqadmin_completion` file from the [releases](https://github.com/jerrysearch/rocketmq-completion/releases) to local directory
* Add the following command to `~/.bash_profile`

```bash
source /path/mqadmin_completion
```
* Log in to the current user or execute `source ~/.bash_profile`
* Check that the script is valid

```bash
complete -p | grep -e mqadmin
```
The following appears in the output as successful

```bash
complete -F _mqadmin mqadmin
```
## Usage

```bash
./mqadmin [tab]
./mqadmin <command> [-tab][--tab]
```

**- Indicates a required parameter
-- Indicates optional parameters**
				
## About upgrading
* Currently only suport mqadmin script , if the increase in the new command support, use the same way
* For individual script updates, download the new script and overwrite the old version

## About the author

Just a coder

## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) Copyright (C) 2015-2017 Jerry


