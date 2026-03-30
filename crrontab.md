# Comandos parra administración de CRON TAB

## Editar
```
crontab -e
```

## Listar tareas
```
crontab -le
```

## Agregar tarea para Schedule
```
* * * * * cd /var/www/nombre && php artisan schedule:run >> /dev/null 2>&1
```

## Agregar tarea para Queue (No rmuy recomendado)
```
* * * * * cd /var/www/nombre && php artisan queue:work --stop-when-empty >> /dev/null 2>&1
```

## Instalar Supervisor: 
```
sudo apt-get install supervisor
```

## Crear archivo de configuración: 
```
sudo nano /etc/supervisor/conf.d/laravel-worker.conf
```

## Contenido:
```
[program:laravel-worker]
process_name=%(program_name)s_%(process_num)02d
command=php /var/www/kleudev/artisan queue:work --sleep=3 --tries=3
autostart=true
autorestart=true
user=root
numprocs=4
redirect_stderr=true
stdout_logfile=/var/www/kleudev/storage/logs/worker.log
```

```
[program:laravel-worker-plataforma-reverb]
process_name =%(program_name)s_%(process_num)02d
command =php /var/www/plataforma/artisan reverb:start
autostart = true
autorestart = true
stopasgroup = true
killasgroup = true
user =www-data
numprocs = 1
redirect_stderr = true
stdout_logfile =/var/www/plataforma/reverb.log
```



## Recargar:
```
sudo supervisorctl reread 
```

## Actualizar:
```
sudo supervisorctl update
```

# Sintaxis de Crontab:

## La estructura consiste en cinco campos de tiempo seguidos por el comando: m h dom mon dow comando 
```
m: Minuto (0-59).
h: Hora (0-23).
dom: Día del mes (1-31).
mon: Mes (1-12).
dow: Día de la semana (0-7, donde 0 y 7 son domingo). 
```

## Comandos útiles:
```
crontab -e: Editar el archivo crontab del usuario.
crontab -l: Listar las tareas programadas.
crontab -r: Eliminar todas las tareas del usuario. 
```

## Caracteres Especiales y Atajos:
```
*: Asterisco, significa "todos" los valores para ese campo.
,: Coma, separa valores individuales.
-: Guion, define un rango de tiempo.
/: Diagonal, expresa valores de paso (ej. */10 cada 10 min).
```
