# Comandos administración Supervisor de procesos

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

## Iniciar procesos
```
sudo supervisorctl start laravel-worker:*
```

# Procesos configurador

## Plataforma
```
laravel-worker-plataforma.conf
```

```
sudo supervisorctl start laravel-worker-plataforma:*
```

```
laravel-worker-plataforma-reverb.conf
```
```
sudo supervisorctl start laravel-worker-plataforma-reverb:*
```

## Trabajos de KLEUDEV
```
laravel-worker-reverb.conf
```
```
sudo supervisorctl start laravel-worker-reverb:*
```
```
laravel-worker.conf
```
```
sudo supervisorctl start laravel-worker:*
```

## Trabajos de KLEUPOS
```
laravel-worker-kleupos.conf
```
```
sudo supervisorctl start laravel-worker-kleupos:*
```
