# config.py

import os

MAX_CONTENT_LENGTH = 8 * 1024 * 1024
ALLOWED_EXTENSIONS = set(['png', 'jpg', 'jpeg', 'gif'])
# upload imag path
UPLOAD_FOLDER=os.getcwd()+"/IMAGEPATH/"
SECRET_KEY = 'catcat'
SESSION_COOKIE_NAME='connect.sid'
#mysql_setting
DATA_BACKEND = 'mysql'
MYSQL_HOST='127.0.0.1'
MYSQL_USER = ''
MYSQL_PASSWORD = ''
MYSQL_DATABASE = 'bookshelf'
#sqlite_setting
SQLITE_PATH=os.getcwd()+"\\bookshelf.db"
SQLALCHEMY_SQLITE_URI = ( 'sqlite:///{path}').format(path=SQLITE_PATH)
SQLALCHEMY_MYSQL_URI = (
    'mysql+pymysql://{user}:{password}@{host}:3306/{database}').format(
        user=MYSQL_USER, password=MYSQL_PASSWORD,host=MYSQL_HOST,
        database=MYSQL_DATABASE)
#DATA_BACKEND{sqlite mysql}        
DATA_BACKEND = 'sqlite'
if DATA_BACKEND=='mysql':
    SQLALCHEMY_DATABASE_URI = SQLALCHEMY_MYSQL_URI
else:
    SQLALCHEMY_DATABASE_URI = SQLALCHEMY_SQLITE_URI

#end config.py



#mysql
my.ini
[mysqld]
basedir=c:/appserv/mysql
datadir=c:/appserv/mysql/data
[mysqld-8.0]
sql_mode=TRADITIONAL

bin\mysqld --defaults-file=my.ini --initialize --console
A temporary password is generated for root@localhost: qk-nm1!hE/4r

mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密碼';

#redis
https://github.com/microsoftarchive/redis/releases

#pip install virtualenv
virtualenv --python "c:\python36\python.exe" env

#pip instal -r requirements.txt
env\scripts\activate
bookshelf>python model_cloudsql.py
python main.py
