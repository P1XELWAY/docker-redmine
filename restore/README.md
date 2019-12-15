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

Open the PhpMyAdmin, select redmine database and put sql content and run the query.