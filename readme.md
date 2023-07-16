## 背景
如果在Windows上开发需要用到php和nginx，需要打开两个终端，并执行命令：**nginx** 和**php-cgi.exe -b 127.0.0.1:9000 -c php.ini**，以上终端不能关闭。
为了优化开发体验，希望以服务的形式安装这两个软件，随着电脑启动而自动运行，不用再单独运行保持命令行窗口打开。
## 安装方法
首先要下载程序包，nginx_php_services.7z
或者
git clone git@github.com:yiaihugongyuan/php_nginx_services.git
在仓库内能找到程序包。
### nginx的安装方法
* 将压缩文件解压到C盘根目录。
* 以管理员身份打开PowerShell，进入ngxin目录。
* 运行 **nginx-server.exe install**，安装服务。
* 运行 **net start nginx** ，启动nginx服务。
### php的安装方法
* 仍然以管理员身份进入php目录。
* 运行 **php-cgi-service install**，安装服务。
* 运行 **net start php-cgi**，启动php-cgi服务。
## 运行环境
* 本方法在Windows 10上成功运行。
* nginx 版本1.8.1。
* php版本 8.2。 
### 修改配置
如果修改了php和nginx的配置文件，需要重新启动服务，修改才生效。
