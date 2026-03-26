#Comandos para admninistración de POSTGRES

## Reiniciar Servidor
```
sudo systemctl restart postgresql
```

## Acceder a servidor
```
sudo -u postgres psql
```

## Consultar información de Postgres
```
SELECT datname FROM pg_database;

SELECT usename FROM pg_user;

SELECT rolname FROM pg_roles;

SELECT rolname, rolsuper, rolcreaterole, rolcreatedb, rolcanlogin FROM pg_roles;

SELECT rolname, rolsuper, rolcreaterole, rolcreatedb, rolcanlogin, rolreplication FROM pg_roles WHERE rolname = 'userkleplataforma';
```

## Crear Base de Datos
```
CREATE DATABASE nombredb;
```

## Crear usuario
```
CREATE USER nombreuser WITH ENCRYPTED PASSWORD 'password';
```

## Asignar privilegios a base de datos y usuario
```
GRANT ALL PRIVILEGES ON DATABASE dbchubb01 TO userkleplataforma;
GRANT pg_read_all_data TO userkleplataforma;
GRANT pg_write_all_data TO userkleplataforma;
```

## Asignar privilegios a usuario para el squema public (No Necesario)
```
GRANT ALL ON SCHEMA public TO nuevousuario;
```

## Conectar a servidor de Postgres
```
psql -h localhost -U nuevousuario -d nombrebasededatos
```

## Importar base de datos 
```
sudo -u postgres psql nombrebasededatos < /home/nombrebasededatos.sql
```

## Exportar base de datos en Window 11 
```
cd C:\Program Files\PostgreSQL\18\bin
```
```
pg_dump -U postgres -d badededatos -f E:\Respaldo_SQL\Postgres\2026\03\20\nombre.sql
```

## Eliminar base de datos 
```
sudo -u postgres dropdb 'dbchubb01'
```

## Eliminar base de datos a través de SQL 
```
DROP DATABASE nombrebasededatos;
```

## Forzar eliminación de base de datos a través de SQL 
```
DROP DATABASE dbchubb01 WITH (FORCE);
```

## Habilitar y Deshabilitar conexión a servidor 
```
ALTER DATABASE dbchubb01 WITH ALLOW_CONNECTIONS = false;
ALTER DATABASE dbchubb01 WITH ALLOW_CONNECTIONS = true;
```

# Administración Postgres en Window
## Ruta a binario de Postgres
```
C:\Program Files\PostgreSQL\18\bin>
```
## Importar base de datos
```
psql -h localhost -U postgres -d dbchubb01 -f "D:\DESARROLLO\RESPALDOS_DB\2026\03\06\dbchubb01.sql"
```
## Exportar base de datos
```
pg_dump -U postgres -d dbchubb01 -f  "D:\DESARROLLO\RESPALDOS_DB\2026\03\06\dbchubb01V3.sql"
```
