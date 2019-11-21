python3 -m virtualenv venv

source venv/bin/activate

pip install django

django-admin startproject todo .

python manage.py startapp app

#install mysql server

sudo apt-get install mysql-server

#open cli

sudo mysql

#start mysql app

sudo systemctl start mysql

#set authenication

UPDATE mysql.user SET authentication_string = PASSWORD('password') WHERE User = 'root';

#apply changes

FLUSH PRIVILEGES;
