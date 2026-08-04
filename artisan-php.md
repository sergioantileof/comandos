# Comandos para adiministración de Artisan en Laravel

## Crear proyecto Laravel
```
composer create-project laravel/laravel nombre-app
```

## Borra la caché de configuración.
```
php artisan config:clear 
```

## Crea la caché de configuración para mejorar el
```
php artisan config:cache 
```


# Migraciones

## Crear tabla

```
php artisan make:migration create_nombre_tabla_table
```
## Agregar campo a tabla

```
php artisan make:migration add_telefono_to_clientes_table --table=clientes
```

## Ejecutarr migración

```
php artisan migrate
```




