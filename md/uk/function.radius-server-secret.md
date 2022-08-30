Повертає загальний секрет

-   [« radiussendrequest](function.radius-send-request.html)
    
-   [radiusstrerror »](function.radius-strerror.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Повертає загальний секрет
    

# radiusserversecret

(PECL radius >= 1.1.0)

radiusserversecret — Повертає загальний секрет

### Опис

```methodsynopsis
radius_server_secret(resource $radius_handle): string
```

Загальний секрет необхідний як сіль для розбирання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає загальний секрет сервера у вигляді рядка або **`false`** у разі виникнення помилки.