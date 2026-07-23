# Comandos administración Supervisor de procesos

## Ruta de los archivos de configuración
```
cd /etc/supervisor/conf.d/
```

## Verificar estado
```
sudo supervisorctl status
```

## Detener Supervisor
```
sudo systemctl stop supervisor
```

## Iniciar Supervisor
```
sudo systemctl start supervisor
```

## Reiniciar Todo
```
sudo supervisorctl restart all
```

## Recarga
```
sudo supervisorctl reread
```

## Actualización
```
sudo supervisorctl update
```

# Procesos configurador

## PLATAFORMA
```
sudo nano /etc/supervisor/conf.d/plataforma-reverb.conf
```
```
sudo nano /etc/supervisor/conf.d/plataforma-queue.conf
```

## KLEUDEV
```
sudo nano /etc/supervisor/conf.d/kleudev-reverb.conf
```
```
sudo nano /etc/supervisor/conf.d/kleudev-queue.conf
```

## KLEUPOS
```
sudo nano /etc/supervisor/conf.d/kleupos-queue.conf
```
