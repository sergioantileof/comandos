# Comandos para administrar dominios en NGINX


## Copiar Archivo por defecto con su configuración
```
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/nuevodominio.com
```

## Editar nuevo archivo de dominio
```
sudo nano /etc/nginx/sites-available/nuevodominio.com

```

## Asignar archivo de dominio
```
sudo ln -s /etc/nginx/sites-available/nuevodominio.com /etc/nginx/sites-enabled/
```

## Verificar la configuración
```
sudo nginx -t
```

## Recargar NGINX
```
sudo systemctl reload nginx
```
