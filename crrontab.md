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

## Recargar:
```
sudo supervisorctl reread 
```

## Actualizar:
```
sudo supervisorctl update
```
