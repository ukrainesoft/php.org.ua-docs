---
navigation:
  - function.imagestringup.html: « imagestringup
  - function.imagesy.html: imagesy »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagesx
---
# imagesx

(PHP 4, PHP 5, PHP 7, PHP 8)

imagesx — Отримання ширини зображення

### Опис

```methodsynopsis
imagesx(GdImage $image): int
```

Повертає ширину зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає ширину зображення `image` або **`false`** у разі помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesx()****

```php
<?php

// создание изображения 300*200
$img = imagecreatetruecolor(300, 200);

echo imagesx($img); // 300

?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення
-   [getimagesize()](function.getimagesize.html) - Отримання розміру зображення
-   [imagesy()](function.imagesy.html) - Отримання висоти зображення
