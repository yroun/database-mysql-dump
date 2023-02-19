## database-mysql-dump

- dump ddl

```
mysqldump --column-statistics=0 \
	--single-transaction --no-data \
	--databases DB_NAME \
	--ignore-table=DB_NAME.TABLE_NAME \
	-hHOST -P3306 -uUSER -p > NAME.sql
```

- dump data

```
mysqldump --column-statistics=0 \
	--single-transaction --no-create-db --no-create-info \
	--databases DB_NAME \
	--ignore-table=DB_NAME.TABLE_NAME \
	-hHOST -P3306 -uUSER -p > NAME.sql
```

- restore

-f : force progress on error

```
mysql -f -hHOST -P3306 -uUSER -p < NAME.sql
```
