---
navigation:
  - function.imagestringup.md: « imagestringup
  - function.imagesy.md: imagesy »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesx
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає ширину зображення `image`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagesx()\*\*\*\*

```php
<?php

// создание изображения 300*200
$img = imagecreatetruecolor(300, 200);

echo imagesx($img); // 300

?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
-   [getimagesize()](function.getimagesize.md) \- Отримання розміру зображення
-   [imagesy()](function.imagesy.md) \- Отримання висоти зображення
