# Comandos para admninistración de MySQL

## Crear Usuario de MySQL
```
CREATE USER 'userkleudev'@'localhost' IDENTIFIED BY 'JHJdlandOIOIDA34+-d';
```

## Crear una base de Dados en MySQL 
```
CREATE DATABASE nombre_de_tu_db;
```

## Asignar Privilegios al Nuevo usuario
```
GRANT ALL PRIVILEGES ON *.* TO 'userkleudev'@'localhost' WITH GRANT OPTION;
```

## Asignar Roles al Usuario
```
GRANT SELECT, INSERT, UPDATE, DELETE ON dbhdc01.* TO 'userkleudev'@'localhost';
```

## Flush
```
FLUSH PRIVILEGES;
```

## Importar Base de Datos a MySQL
```
mysql -u root -p dbhdc01 < /home/hdc.sql
mysql -u root -p dbgastos01 < /home/antileoc_sergio.sql
```

## Editar archivo de configuración de MySQL
```
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```
