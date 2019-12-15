# docker-redmine
Docker compose with Redmine/PhpMyAdmin/Mysql

### To start new instance of Docker

```
chmod +x compose
./compose up
```

### Detail :

./files     -   Redirection files of all attachments on issues

./themes    -   Redirection themes to apply customizations

./restore   -   How to migrate Redmine SQLITE 3 database

./env       -   Database and redmine configuration


### Access :

Redmine     -   http://*.*.*.*:32768

MySQL       -   *.*.*.*:3306

PhpMyAdmin  -   http://*.*.*.*:8000

To change the port, update the docker-compose.yml.