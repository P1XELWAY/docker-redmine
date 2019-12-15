# Sqlite3 migration

### Prerequist

```
apt install sqlite3
chmod +x sqlite3-to-mysql.py
```

### Command to convert sqlite3 database to mysql database :

```
sqlite3 redmine.db .dump | ./sqlite3-to-mysql.py -u redmine -p redmine -d redmine > redmine.db.sql
```

### MySQL import :

Open the PhpMyAdmin, select redmine database and put sql content and run the query

### After a sqlite migration :

To fix add ISSUES add auto increment on ID column of table issues with phpmyadmin

To debug Redmine open the file '/usr/src/redmine/config' and add :

To log inside the STDOUT of Portainer.IO :

```
config.logger = Logger.new(STDOUT)
```

To log in debug.log file :

```
#Logger.new(PATH,NUM_FILES_TO_ROTATE,FILE_SIZE)
config.logger = Logger.new('/usr/src/redmine/log/debug.log', 2, 1000000)
config.logger.level = Logger::INFO
```
