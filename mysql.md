# Comandos para admninistración de MySQL

## Conectar a MySQL
```
sudo mysql -u root -p
```

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

# Conexiones Window
## Ruta acceso al binario de MySQL
```
C:\xampp\mysql\bin
```
## Crear base de datos MySQL
```
mysql -u root -e "create database dbalgo01"
```
## Importar base dedatos de MySQL
```
mysql -u root -p dbsura01 < "E:\Respaldo_SQL\2026\03\10\sura.sql"
```
## Exportar base de datos de MySQL
```
mysqldump -u root -p dbchubb01 > "D:\DESARROLLO\RESPALDOS_DB\2026\03\06\dbchubb01.sql"
```
