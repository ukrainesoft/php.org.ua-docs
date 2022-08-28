Відкриває зображення з файлу

-   [« ps\_open\_file](function.ps-open-file.html)
    
-   [ps\_open\_image »](function.ps-open-image.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Відкриває зображення з файлу
    

# псopenimagefile

(PECL ps >= 1.1.0)

псopenimagefile — Відкриває зображення з файлу

### Опис

```methodsynopsis
ps_open_image_file(    resource $psdoc,    string $type,    string $filename,    string $stringparam = ?,    int $intparam = 0): int
```

Завантажує зображення для подальшого використання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`type`

Тип зображення. Можливі значення: `png` `jpeg` або `eps`

`filename`

Ім'я файлу, який містить дані зображення.

`stringparam`

Параметр не використовується.

`intparam`

Параметр не використовується.

### Значення, що повертаються

Повертає ідентифікатор зображення або нуль у разі помилки. Ідентифікатор – позитивне число більше 0.

### Дивіться також

-   [ps\_open\_image()](function.ps-open-image.html) - Зчитує зображення для подальшого розміщення
-   [ps\_place\_image()](function.ps-place-image.html) - Розміщує зображення на сторінці
-   [ps\_close\_image()](function.ps-close-image.html) - Закриває зображення та звільняє пам'ять