Повертає аутентифікатор запиту

-   [« radius\_put\_vendor\_string](function.radius-put-vendor-string.html)
    
-   [radius\_salt\_encrypt\_attr »](function.radius-salt-encrypt-attr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Повертає аутентифікатор запиту
    

# radiusrequestauthenticator

(PECL radius >= 1.1.0)

radiusrequestauthenticator — Повертає автентифікатор запиту

### Опис

```methodsynopsis
radius_request_authenticator(resource $radius_handle): string
```

Аутентифікатор запиту необхідний для розпізнавання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає автентифікатор запиту у вигляді рядка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [radius\_demangle()](function.radius-demangle.html) - Розшифровує дані