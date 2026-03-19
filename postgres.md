#Comandos para admninistración de POSTGRES

## Reiniciar Servidor
```
sudo systemctl restart postgresql
```

## Acceder a servidor
```
sudo -u postgres psql
```

## Crear usuarios
```
CREATE USER nuevousuario WITH PASSWORD 'definirpassword';
```

## Crear usuarios
```
CREATE DATABASE nombrebasededatos OWNER nuevousuario;
```

## Asignar privilegios a base de datos y usuario
```
GRANT ALL PRIVILEGES ON DATABASE nombrebasededatos TO nuevousuario;
```

## Asignar privilegios a usuario para el squema public
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


