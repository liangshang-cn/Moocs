vim mcd.sh

> mcd() {
>
> ​	mkdir -p "$1"
>
> ​	cd "$1"
>
> }

source mcd.sh

mcd test 

其中source命令将mcd程序加载到了shell的查找路径中； mcd test用test替换掉了$1中的1，所以新建的是名为mcd的文件夹（$1表示脚本的第一个参数，而$0表示脚本名本身，$?从上一条命令中获取错误代码，$_表示最后一个参数）。另一个常用的替换是用!!替换上一条命令

将命令的输出作为变量

foo=$(pwd)

echo "we are in $foo"

