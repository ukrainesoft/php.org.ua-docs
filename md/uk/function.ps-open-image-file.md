---
navigation:
  - function.ps-open-file.md: « ps\_open\_file
  - function.ps-open-image.md: ps\_open\_image »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_open\_image\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_open\_image\_file

(PECL ps >= 1.1.0)

ps\_open\_image\_file — Відкриває зображення з файлу

### Опис

```methodsynopsis
ps_open_image_file(    resource $psdoc,    string $type,    string $filename,    string $stringparam = ?,    int $intparam = 0): int
```

Завантажує зображення для подальшого використання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`type`

Тип зображення. Можливі значення: `png` `jpeg`или`eps`

`filename`

Ім'я файлу, який містить дані зображення.

`stringparam`

Параметр не використовується.

`intparam`

Параметр не використовується.

### Значення, що повертаються

Повертає ідентифікатор зображення або нуль у разі помилки. Ідентифікатор – позитивне число більше 0.

### Дивіться також

-   [ps\_open\_image()](function.ps-open-image.md) \- Зчитує зображення для подальшого розміщення
-   [ps\_place\_image()](function.ps-place-image.md) \- Розміщує зображення на сторінці
-   [ps\_close\_image()](function.ps-close-image.md) \- Закриває зображення та звільняє пам'ять
