#课霸

校园专属课程交流与换课多功能平台

##Dependency

-   [Git](https://git-scm.com/)
-	[Django](https://www.djangoproject.com/)
-	[Mysql](https://www.mysql.com/)

##Setup

1、安装MYSQL

2、安装Python和pip

3、通过pip安装Django(Version1.8.1)，MySQL-python(Version1.2.3)

4、在MySQL命令行创建数据库 ```create database keba default character set utf8 collate utf8_bin;```

5、在src/Sysulesson/setting.py 文件中修改数据库信息（包括数据库名称以及密码）；

6、在src目录下执命令 ```python manage.py makemigrations``` ```python manage.py migrate```

7、在Mysql中执行 ```use sysu_lesson;```   ```source xxx.mysql```导入数据；

8、启动```python manage.py runserver 0.0.0.0:8888``` （端口可自行设置)

9、用教务系统账号登陆； =。=

***

若正确运行，将显示如下信息：
> Performing system checks...
> 
> System check identified no issues (0 silenced).
> July 18, 2015 - 10:24:26
> Django version 1.8.2, using settings 'SysuLesson.settings'
> Starting development server at http://127.0.0.1:8000/
> Quit the server with CONTROL-C.

##FAQ
- django.db.utils.OperationalError: (2002, "Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (2)")

    Start your mysql service by typing ```sudo service mysql start``` in your terminal.

- django.db.utils.OperationalError: (1045, "Access denied for user 'root'@'localhost' (using password: YES)")

    Modify database setting in src/SysuLesson/settings.py, especially the user and password.

- Unable to access from other devices.

    Check whether you have added ```0.0.0.0:[PORT]``` in your command or not.
