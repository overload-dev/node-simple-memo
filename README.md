using express-generator.<br>
mysql connection sample project

<pre>
<code>
$ mysql -u root -p

mysql> CREATE DATABASE NODE_DB;
mysql> USE NODE_DB;
mysql> CREATE TABLE MEMOS(
  -> ID INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  -> CONTENT VARCHAR(500) CHARACTER SET UTF8 NOT NULL,
  -> CREATED_AT TIMESTAMP NULL DEFAULT NULL,
  -> UPDATED_AT TIMESTAMP NULL DEFAULT NULL);
  

mysql> INSERT INTO MEMOS(CONTENT, CREATED_AT, UPDATED_AT)
  -> VALUES('TEXT 1', NOW(), NOW()),
  -> ('TEXT 2', NOW(), NOW()),
  -> ('TEXT 3', NOW(), NOW()),
  -> ('TEXT 4', NOW(), NOW());

---
mysql> SELECT * FROM MEMOS;
+----+---------+---------------------+---------------------+
| ID | CONTENT | CREATED_AT          | UPDATED_AT          |
+----+---------+---------------------+---------------------+
|  1 | TEXT 1  | 2020-03-17 20:34:17 | 2020-03-17 20:34:17 |
|  2 | TEXT 2  | 2020-03-17 20:34:17 | 2020-03-17 20:34:17 |
|  3 | TEXT 3  | 2020-03-17 20:34:17 | 2020-03-17 20:34:17 |
|  4 | TEXT 4  | 2020-03-17 20:34:17 | 2020-03-17 20:34:17 |
+----+---------+---------------------+---------------------+

mysql> FLUSH PRIVILEGES;
mysql> EXIT;
</code>
</pre>