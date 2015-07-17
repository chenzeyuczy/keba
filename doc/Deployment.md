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
The command above will run server on local machine which can only be visited locally. To make it possible for other devices to access the website, input the following command instead.
```
python manage.py runserver 0.0.0.0:[PORT]
```