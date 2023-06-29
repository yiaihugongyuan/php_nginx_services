# Windows 10系统下将Nginx和PHP以服务形式安装

## 背景
* 默认情况下，在Windows运行Nginx和PHP组合，分别要用命令行形式打开Nginx和php-cgi.exe -b 127.0.0.1:9000 -c php.ini，并且不能关闭窗口，造成不便。安装成服务服务形式就可以解决这个问题。随着电脑启动而自动运行，不再保持命令行窗口打开。
## 安装方法
### nginx的安装方法
* 将压缩文件解压到C盘根目录。
* 以管理员身份打开PowerShell，进入ngxin目录。
* 运行 **nginx-server.exe install**，安装服务。
* 运行 **net start nginx** ，启动nginx服务。
### php的安装方法
* 仍然以管理员身份进入php目录。
* 运行 **php-cgi-service install**，安装服务。
* 运行 ** net start php-cgi**，启动php-cgi服务。
## 运行环境
* 本方法在Windows 10上成功运行。
* nginx 版本1.8.1。
* php版本 8.2。 