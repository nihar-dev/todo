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

# sql query
CREATE TABLE Users (
    ID int NOT NULL,
    Name varchar(255) NOT NULL,
    Email varchar(255),
    PRIMARY KEY (ID)
);

CREATE TABLE Todo (
    ID int NOT NULL auto_increment primary key,
    BucketId int NOT NULL ,
    UserId int NOT NULL references Users(ID),
    Todo varchar(255) NOT NULL,
    BucketName varchar(255) NOT NULL,
    Status int NOT NULL
);
