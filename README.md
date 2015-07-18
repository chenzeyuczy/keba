#课霸

选最水的课！

##Setup

1、安装MYSQL

2、安装Python和pip

3、通过pip安装Django(Version1.8.1)，MySQL-python(Version1.2.3)

4、在MySQL命令行创建数据库 ```create database keba default character set utf8 collate utf8_bin;```

5、在src/Sysulesson/setting.py 文件中修改数据库信息（包括数据库名称以及密码）；

6、在src目录下执命令 ```python manage.py makemigrations``` ```python manage.py migrate```

7、在Mysql中执行 ```use keba;```   ```source xxx.mysql```导入数据；

8、启动```python manage.py runserver 0.0.0.0:8888``` （端口可自行设置)

9、用教务系统账号登陆； =。=
