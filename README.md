# 微聊
本系统是基于easyswoole开发的聊天室系统,实现了登陆、退出、选择聊天室、向某个聊天室内的某个成员发起私聊、和全体成员聊天。<br>
本系统代码简洁，非常适合初学者学习swoole和easyswoole。<br>
开发环境:swoole2.x、easyswoole2.x、redis3.x、Mysql5.7、PHP7.1+、Nginx<br>
安装步骤:<br>
　　1、安装PHP，给php安装swoole2.x扩展<br>
　　2、安装Mysql、Redis、Nginx,将根目录下的easyswoole.sql导入到mysql<br>
　　3、配置Nginx<br>
　　server {<br>
　　　client_max_body_size 8M;<br>
　　　listen       80;<br>
　　　server_name 这里改成你自己的IP或域名;<br>
　　　root 项目路径;<br>
　　　index index.html index.htm index.php;<br>
　　　location / {<br>
　　　　if (!-e $request_filename){<br>
　　　　　　　proxy_pass http://127.0.0.1:9501;<br>
　　　　　　}<br>
　　　　}<br>
　　}<br>
　　4、安装easyswoole，进入根目录下执行 php composer.phar require easyswoole/easyswoole=2.x-dev<br>
　　5、执行 php vendor/bin/easyswoole install 选择N 不要覆盖配置文件<br>
　　6、安装MysqlDb扩展 php composer.phar require joshcam/mysqli-database-class:dev-master<br>
　　7、修改根目录下Config.php Redis和Mysql的配置<br>
　　8、Public/static/js/common.js下面的baseUrl改为你的域名或IP<br>
　　9、进入根目录 php easyswoole start 启动项目<br>
目前还没有开发用户注册功能,如需添加账户可以自己在wl_member表中添加。<br>
初始化账户:18588888888、18577777777、185666666666密码都是123456<br>
如有问题，欢迎大家和我一起交流学习。<br>
开发者:<br>
　许鹏亮 11468804@qq.com<br>