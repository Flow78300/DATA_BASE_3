# DATA_BASE_3
exo db 3


mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| kamelott           |
| mysql              |
| performance_schema |
| sys                |
| wild               |
| wild_db_quest      |
+--------------------+
7 rows in set (0,04 sec)

mysql> USE wild_db_quest;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> SHOW TABLES;
+-------------------------+
| Tables_in_wild_db_quest |
+-------------------------+
| school                  |
| wizard                  |
+-------------------------+
2 rows in set (0,00 sec)

mysql> INSERT INTO school (name, country, capacity) VALUES ('Beauxbatons Academy of Magic', 'France', 550), ('Castelobruxo', 'Brazil', 380), ('Durmstrang Institute', 'Norway', 570), ('Hogwarts School of Witchcraft and Wizardry', 'United Kingdom', ' 450'), ('Ilvermorny School of Witchcraft and Wizardry', 'USA', '300'), ('Koldovstoretz', 'Russia', '125'), ('Mahoutokoro School of Magic', 'Japan', '800'), ('Uagadou School of Magic', 'Uganda', '350');
Query OK, 8 rows affected (2,09 sec)
Records: 8  Duplicates: 0  Warnings: 0

mysql> UPDATE school SET country = 'Sweden' WHERE id = 3;
Query OK, 1 row affected (5,60 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> UPDATE school SET capacity = 700 WHERE id = 7;
Query OK, 1 row affected (1,03 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> DELETE FROM school WHERE name LIKE '%gic';
Query OK, 3 rows affected (1,02 sec)

mysql> SELECT * FROM school;
+----+----------------------------------------------+----------+----------------+
| id | name                                         | capacity | country        |
+----+----------------------------------------------+----------+----------------+
|  2 | Castelobruxo                                 |      380 | Brazil         |
|  3 | Durmstrang Institute                         |      570 | Sweden         |
|  4 | Hogwarts School of Witchcraft and Wizardry   |      450 | United Kingdom |
|  5 | Ilvermorny School of Witchcraft and Wizardry |      300 | USA            |
|  6 | Koldovstoretz                                |      125 | Russia         |
+----+----------------------------------------------+----------+----------------+
5 rows in set (0,07 sec)

mysql> 
