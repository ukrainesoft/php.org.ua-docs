---
navigation:
  - function.ps-open-file.md: «psopenfile
  - function.ps-open-image.md: псopenimage »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псopenimagefile
---
# псopenimagefile

(PECL ps >= 1.1.0)

псopenimagefile — Відкриває зображення з файлу

### Опис

```methodsynopsis
ps_open_image_file(    resource $psdoc,    string $type,    string $filename,    string $stringparam = ?,    int $intparam = 0): int
```

Завантажує зображення для подальшого використання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

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

-   [псopenimage()](function.ps-open-image.md) - Зчитує зображення для подальшого розміщення
-   [псplaceimage()](function.ps-place-image.md) - Розміщує зображення на сторінці
-   [псcloseimage()](function.ps-close-image.md) - Закриває зображення та звільняє пам'ять
