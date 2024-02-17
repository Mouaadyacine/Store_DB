
mysql> create database storeDB;
Query OK, 1 row affected (0.1 sec)

mysql> use storeDB;
Database changed
mysql> create table client (
    ->     clientID int not null,
    ->     name varchar(14) not null ,
    ->     email varchar(14) not null,
    ->     adresse varchar(14) not null,
    ->     primary key(clientID)
    -> );
Query OK, 0 rows affected (0.4 sec)

mysql>
mysql> create table produit (
    ->     produitID int not null,
    ->     nom varchar(16) not null,
    ->     descr varchar(16) not null,
    ->     prix int ,
    ->     stock int,
    ->     primary key (produitID),
    -> );
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ')' at line 8
mysql>
mysql> create table commande (
    ->     commandeID int not null,
    ->     statut varchar(14) not null  default "en cours" check (statut in ("en cours ","livree", "annulee"))  ,
    ->     total varchar(14) not null,
    ->     primary key(commandeID),
    ->     clientID int,
    ->     foreign key (clientID) references client(clientID)
    ->
    -> );
Query OK, 0 rows affected (0.5 sec)

mysql> show tables;
+-------------------+
| Tables_in_storedb |
+-------------------+
| client            |
| commande          |
+-------------------+
2 rows in set (0.00 sec)

mysql>
mysql> create table produit (
    ->     produitID int not null,
    ->     nom varchar(16) not null,
    ->     descr varchar(16) not null,
    ->     prix int ,
    ->     stock int,
    ->     primary key (produitID)
    -> );
Query OK, 0 rows affected (0.4 sec)

mysql> show tables;
+-------------------+
| Tables_in_storedb |
+-------------------+
| client            |
| commande          |
| produit           |
+-------------------+
3 rows in set (0.01 sec)

mysql> desc commande;
+------------+-------------+------+-----+----------+-------+
| Field      | Type        | Null | Key | Default  | Extra |
+------------+-------------+------+-----+----------+-------+
| commandeID | int         | NO   | PRI | NULL     |       |
| statut     | varchar(14) | NO   |     | en cours |       |
| total      | varchar(14) | NO   |     | NULL     |       |
| clientID   | int         | YES  | MUL | NULL     |       |
+------------+-------------+------+-----+----------+-------+
4 rows in set (0.07 sec)

mysql>