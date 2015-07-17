#Deployment Instruction#


###Dependency###
- [Git](https://git-scm.com/)
- [Django](https://www.djangoproject.com/)
- [Mysql](https://www.mysql.com/)


###Tutorial###
- Clone from [project page](https://github.com/chenzeyuczy/keba).
```
git clone https://github.com/chenzeyuczy/keba.git
```
- Enter directory.
```
cd keba/src/
```
- Migrate applications.
```
python manage.py migrate
```
- Run server.
```
python manage.py runserver
```
The command above will run server on local machine which can only be visited locally. To make it accessible for other devices, input the following command instead.
```
python manage.py runserver 0.0.0.0:[PORT]
```

If everything goes in a proper way, you'll see something like this.
> Performing system checks...
> 
> System check identified no issues (0 silenced).
> July 18, 2015 - 10:24:26
> Django version 1.8.2, using settings 'SysuLesson.settings'
> Starting development server at http://127.0.0.1:8000/
> Quit the server with CONTROL-C.
> ...

###FAQ###
- django.db.utils.OperationalError: (2002, "Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (2)")

Start your mysql service by typing ```sudo service mysql start``` in your terminal.

- django.db.utils.OperationalError: (1045, "Access denied for user 'root'@'localhost' (using password: YES)")

Modify database setting in src/SysuLesson/settings.py, especially the user and password.

- Unable to access from other devices.

Check whether you have added ```0.0.0.0:[PORT]``` in your command or not.