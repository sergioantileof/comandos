# Comandos para administración de LINUX

## Dirigirse hacia una ruta
```
cd /var/www/html
```

## Reinicia servicios
```
sudo systemctl restart nginx
sudo systemctl restart php8.3-fpm
sudo systemctl restart mysql
```

## Cambiar permisos a un directorio
```
sudo chmod -R 777 /var/www/html/carpeta
```

## Asegúrate de permitir SSH 
```
sudo ufw status Status: inactive (no filtra tráfico)
sudo ufw enable. 
sudo ufw allow ssh
```

## Crear nuevo directorio
```
sudo mkdir /var/www/kleudev
```

## Asignar al usuario a la ruta definida
```
sudo chown -R $USER:$USER /var/www/kleudev
```

## Eliminar directorios
```
sudo rm -r /var/www/kleudev
sudo rm -r /var/www/html/mi-app
```

## Mover directorios
```
sudo mv /var/www/html /var/www/html/gastos
```

##  Mover y renombrar: 
```
sudo mv carpeta_original /ruta/destino/nuevo_nombre.
```

## Sobrescribir si existe: 
```
sudo mv -f carpeta /tmp.
```

## No sobrescribir: 
```
sudo mv -n carpeta /tmp.
```

# Instalar certificado https en vps contabo vps

## Método 1: Certbot (Let's Encrypt) - Recomendado (Gratis)

```
Este método es ideal si tienes un VPS con Ubuntu/Debian/CentOS sin panel de control.

Conéctate a tu VPS: Usa SSH (con herramientas como PuTTY).
```

## Instala Certbot:
```
Para Nginx: sudo apt install certbot python3-certbot-nginx.

Para Apache: sudo apt install certbot python3-certbot-apache.
```

## Obtén el certificado:
```
Nginx: sudo certbot --nginx.
Apache: sudo certbot --apache.
```

