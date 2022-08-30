Звільняє всі ресурси

-   [« radiusauthopen](function.radius-auth-open.html)
    
-   [radiusconfig »](function.radius-config.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Звільняє всі ресурси
    

# radiusclose

(PECL radius >= 1.1.0)

radiusclose - Звільняє всі ресурси

### Опис

```methodsynopsis
radius_close(resource $radius_handle): bool
```

Не потрібно викликати цю функцію, тому що PHP звільняє всі ресурси в кінці кожного запиту.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.