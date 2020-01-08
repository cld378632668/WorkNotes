## 前言

```
酷壳以前也写过一些，如《你可能不知道的Shell》和《 应该知道的Linux技巧》，但是Unix/Linux Shell就是一个大宝库，怎么写也写不完，不然，怎么会有“Where is the Shell, there is a way”。

精彩啊。GitHub 找 awesome-shell 。

```

## 脚本库

```
你还可以使用ShellCheck 来帮助你检查你的脚本。
	• https://www.shellcheck.net/
最后推荐一些 Shell 和脚本的参考资料。
各种有意思的命令拼装，一行命令走天涯:
	• http://www.bashoneliners.com/
	• http://www.shell-fu.org/
	• http://www.commandlinefu.com/
下面是一些脚本集中营，你可以在里面淘到各种牛X的脚本：
	• http://www.shelldorado.com/scripts/
	• https://snippets.siftie.com/public/tag/bash/
	• https://bash.cyberciti.biz/
	• https://github.com/alexanderepstein/Bash-Snippets
	• https://github.com/miguelgfierro/scripts
	• https://github.com/epety/100-shell-script-examples
	• https://github.com/ruanyf/simple-bash-scripts
甚至写脚本都可以使用框架:
	• 写bash脚本的框架 https://github.com/Bash-it/bash-it
Google的Shell脚本的代码规范：
	• https://google.github.io/styleguide/shell.xml
最后，别忘了几个和shell有关的索引资源：
	• https://github.com/alebcay/awesome-shell
	• https://github.com/awesome-lists/awesome-bash
	• https://terminalsare.sexy/
最后，如果你还有什么别的更好的玩的东西，欢迎在评论区留言，或是到 coolshellx/ariticles @ github 修改本文。

```

### 命令行

## alias

```
可以参考如下的一些文章，看看别人是怎么用好 alias 的
	• 30 Handy Bash Shell Aliases For Linux / Unix / Mac OS X
	• What are your favorite bash aliases?
	• 23 Handy Bash Shell Aliases For Unix, Linux, and Mac OS X
	• A few more of my favorite Bash aliases
```

## 命令增强

```
下面罗列一些很不错的命令，把原生的命令增强地很厉害:
	• fasd 增强了 cd 命令 。
	• bat 增强了 cat 命令 。如果你想要有语法高亮的 cat，可以试试 ccat 命令。
	• exa 增强了 ls 命令，如果你需要在很多目录上浏览各种文件 ，ranger 命令可以比 cd 和 cat 更有效率，甚至可以在你的终端预览图片。
	• fd 是一个比 find 更简单更快的命令，他还会自动地忽略掉一些你配置在 .gitignore 中的文件，以及 .git 下的文件。
	• fzf 会是一个很好用的文件搜索神器，其主要是搜索当前目录以下的文件，还可以使用 fzf --preview 'cat {}'边搜索文件边浏览内容。
	• grep 是一个上古神器，然而，ack、ag 和 rg 是更好的grep，和上面的 fd一样，在递归目录匹配的时候，会使用你配置在 .gitignore 中的规则。
	• rm 是一个危险的命令，尤其是各种 rm -rf …，所以，trash 是一个更好的删除命令。
	• man 命令是好读文档的命令，但是man的文档有时候太长了，所以，你可以试试 tldr命令，把文档上的一些示例整出来给你看。
	• 如果你想要一个图示化的ping，你可以试试 prettyping 。
	• 如果你想搜索以前打过的命令，不要再用 Ctrl +R 了，你可以使用加强版的 hstr  。
	• htop  是 top 的一个加强版。然而，还有很多的各式各样的top，比如：用于看IO负载的 iotop，网络负载的 iftop, 以及把这些top都集成在一起的 atop。
	• ncdu  比 du 好用多了用。另一个选择是 nnn。
	• 如果你想把你的命令行操作建录制成一个 SVG 动图，那么你可以尝试使用 asciinema 和 svg-trem 。
	• httpie 是一个可以用来替代 curl 和 wget 的 http 客户端，httpie 支持 json 和语法高亮，可以使用简单的语法进行 http 访问: http -v github.com。
	• tmux 在需要经常登录远程服务器工作的时候会很有用，可以保持远程登录的会话，还可以在一个窗口中查看多个 shell 的状态。
	• Taskbook 是可以完全在命令行中使用的任务管理器 ，支持 ToDo 管理，还可以为每个任务加上优先级。
	• sshrc 是个神器，在你登录远程服务器的时候也能使用本机的 shell 的 rc 文件中的配置。
	• goaccess  这个是一个轻量级的分析统计日志文件的工具，主要是分析各种各样的 access log。
关于这些增加命令，主要是参考自下面的这些文章
	1. 10 Tools To Power Up Your Command Line
	2. 5 More Tools To Power Up Your Command Line (Part 2 Of Series)
	3. Power Up Your Command Line, Part 3
	4. Power Up Your Command Line
	5. Hacker Tools
```

# Shell相比Python的优势

```

	• 其一，如果你有一天要维护线上机器的时候，或是到了银行用户的系统（与外网完全隔离，而且服务器上没有安装 Python/PHP 或是他们的的高级库，那么，你只有 Shell 可以用了）。
	• 其二，而且，如果要跟命令行交互很多的话，Shell 是不二之选，试想一下，如果你要去 100 台远程的机器上查access.log 日志中有没有某个错误，完成这个工作你是用 PHP/Python 写脚本快还是用 Shell 写脚本快呢？

```

#  zsh + oh-my-zsh + zsh-autosuggestions  和 fish

fish 也是另外一个牛逼的shell，比如：命令行自动完成（根据历史记录），命令行命令高亮，当你要输入命令行参数的时候，自动提示有哪些参数…… fish在很多地方也是用起来很爽的。和上面的 oh-my-zsh 有点不分伯仲了。


# 写脚本的技巧（慢慢都要掌握的）

```
处理命令行参数的一个样例
1	while [ "$1" != "" ]; do
2	    case $1 in
3	        -s  )   shift  
4	        SERVER=$1 ;;  
5	        -d  )   shift
6	        DATE=$1 ;;
7	    --paramter|p ) shift
8	        PARAMETER=$1;;
9	        -h|help  )   usage # function call
10	                exit ;;
11	        * )     usage # All other parameters
12	                exit 1
13	    esac
14	    shift
15	done
命令行菜单的一个样例
1	#!/bin/bash
2	# Bash Menu Script Example
3	 
4	PS3='Please enter your choice: '
5	options=("Option 1" "Option 2" "Option 3" "Quit")
6	select opt in "${options[@]}"
7	do
8	    case $opt in
9	        "Option 1")
10	            echo "you chose choice 1"
11	            ;;
12	        "Option 2")
13	            echo "you chose choice 2"
14	            ;;
15	        "Option 3")
16	            echo "you chose choice $REPLY which is $opt"
17	            ;;
18	        "Quit")
19	            break
20	            ;;
21	        *) echo "invalid option $REPLY";;
22	    esac
23	done
颜色定义，你可以使用 echo -e "${Blu}blue ${Red}red ${RCol}etc...." 进行有颜色文本的输出
1	RCol='\e[0m'    # Text Reset
2	 
3	# Regular           Bold                Underline           High Intensity      BoldHigh Intens     Background          High Intensity Backgrounds
4	Bla='\e[0;30m';     BBla='\e[1;30m';    UBla='\e[4;30m';    IBla='\e[0;90m';    BIBla='\e[1;90m';   On_Bla='\e[40m';    On_IBla='\e[0;100m';
5	Red='\e[0;31m';     BRed='\e[1;31m';    URed='\e[4;31m';    IRed='\e[0;91m';    BIRed='\e[1;91m';   On_Red='\e[41m';    On_IRed='\e[0;101m';
6	Gre='\e[0;32m';     BGre='\e[1;32m';    UGre='\e[4;32m';    IGre='\e[0;92m';    BIGre='\e[1;92m';   On_Gre='\e[42m';    On_IGre='\e[0;102m';
7	Yel='\e[0;33m';     BYel='\e[1;33m';    UYel='\e[4;33m';    IYel='\e[0;93m';    BIYel='\e[1;93m';   On_Yel='\e[43m';    On_IYel='\e[0;103m';
8	Blu='\e[0;34m';     BBlu='\e[1;34m';    UBlu='\e[4;34m';    IBlu='\e[0;94m';    BIBlu='\e[1;94m';   On_Blu='\e[44m';    On_IBlu='\e[0;104m';
9	Pur='\e[0;35m';     BPur='\e[1;35m';    UPur='\e[4;35m';    IPur='\e[0;95m';    BIPur='\e[1;95m';   On_Pur='\e[45m';    On_IPur='\e[0;105m';
10	Cya='\e[0;36m';     BCya='\e[1;36m';    UCya='\e[4;36m';    ICya='\e[0;96m';    BICya='\e[1;96m';   On_Cya='\e[46m';    On_ICya='\e[0;106m';
11	Whi='\e[0;37m';     BWhi='\e[1;37m';    UWhi='\e[4;37m';    IWhi='\e[0;97m';    BIWhi='\e[1;97m';   On_Whi='\e[47m';    On_IWhi='\e[0;107m';
取当前运行脚本绝对路径的示例：（注：Linux下可以用 dirname $(readlink -f $0) ）
1	FILE="$0"
2	while [[ -h ${FILE} ]]; do
3	    FILE="`readlink "${FILE}"`"
4	done
5	pushd "`dirname "${FILE}"`" > /dev/null
6	DIR=`pwd -P`
7	popd > /dev/null
如何在远程服务器运行一个本地脚本
1	#无参数
2	ssh user@server 'bash -s' < local.script.sh
3	 
4	#有参数
5	ssh user@server ARG1="arg1" ARG2="arg2" 'bash -s' < local_script.sh
如何检查一个命令是否存在，用 which 吗？最好不要用，因为很多操作系统的 which 命令没有设置退出状态码，这样你不知道是否是有那个命令。所以，你应该使用下面的方式。
1	# POSIX 兼容:
2	command -v [the_command]
3	 
4	# bash 环境:
5	hash [the_command]
6	type [the_command]
7	 
8	# 示例：
9	gnudate() {
10	    if hash gdate 2> /dev/null; then
11	        gdate "$@"
12	    else
13	        date "$@"
14	    fi
15	}
然后，如果要写出健壮性更好的脚本，下面是一些相关的技巧：
	• 使用 -e 参数，如：set -e 或是 #!/bin/sh -e，这样设置会让你的脚本出错就会停止运行，这样一来可以防止你的脚本在出错的情况下还在拼拿地干活停不下来。
	• 使用 -u 参数，如： set -eu，这意味着，如果你代码中有变量没有定义，就会退出。
	• 对一些变理，你可以使用默认值。如：${FOO:-'default'}
	• 处理你代码的退出码。这样方便你的脚本跟别的命令行或脚本集成。
	• 尽量不要使用 ; 来执行多个命令，而是使用 &&，这样会在出错的时候停止运行后续的命令。
	• 对于一些字符串变量，使用引号括起，避免其中有空格或是别的什么诡异字符。
	• 如果你的脚有参数，你需要检查脚本运行是否带了你想要的参数，或是，你的脚本可以在没有参数的情况下安全的运行。
	• 为你的脚本设置 -h 和 --help 来显示帮助信息。千万不要把这两个参数用做为的功能。
	• 使用 $() 而不是 “ 来获得命令行的输出，主要原因是易读。
	• 小心不同的平台，尤其是 MacOS 和 Linux 的跨平台。
	• 对于 rm -rf 这样的高危操作，需要检查后面的变量名是否为空，比如：rm -rf $MYDIDR/* 如果 $MYDIR为空，结果是灾难性的。
	• 考虑使用 “find/while” 而不是 “for/find”。如：for F in $(find . -type f) ; do echo $F; done 写成 find . -type f | while read F ; do echo $F ; done 不但可以容忍空格，而且还更快。
	• 防御式编程，在正式执行命令前，把相关的东西都检查好，比如，文件目录有没有存在。
```


