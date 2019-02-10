## ubuntu 常见问题

####  1、 ‘could not get lock /var/cache/apt/archives/lock'

> 解决办法是：
>
> 'sudo rm -rf /var/cache/apt/archieves/lock'
>
> 'sudo apt update'
>
> 这样就可以解决啦

#### 2、ubuntu 安装软件出现 'dpkg status database is locked by another process'

> 解决办法是：
>
> 'sudo rm /var/lib/dpkg/lock'
>
> 'sudo dpkg --configure -a'
>
> 这样就可以解决啦

#### 3、对于gedit  3.X的版本显示中文乱码的问题

> 命令方式：
>
> 'gsettings set org.gnome.gedit.preferences.encodings auto-detected "['GB18030', 'UTF-8', 'CURRENT', 'ISO-8859-15', 'UTF-16']"'
>
> 官网上给出的是这个命令，但是运行命令的时候出现：
>
> 'No such key 'auto-detected'
>
> 在终端下输入'dconf-editor'找到encodings来查看，确实键值已经改了，只需将上面的'auto-detected'改为'candidate-encodings'即可
>
> ' gsettings set org.gnome.gedit.preferences.encodings  candidate-encodings "['GB18030', 'UTF-8', 'CURRENT', 'ISO-8859-15', 'UTF-16']" '

