---
navigation:
  - function.imagesx.md: « imagesx
  - function.imagetruecolortopalette.md: imagetruecolortopalette »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagesy

(PHP 4, PHP 5, PHP 7, PHP 8)

imagesy — Отримання висоти зображення

### Опис

```methodsynopsis
imagesy(GdImage $image): int
```

Повертає висоту заданого зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає висоту зображення `image`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagesy()\*\*\*\*

```php
<?php

// Создание изображения 300*200
$img = imagecreatetruecolor(300, 200);

echo imagesy($img); // 200

?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
-   [getimagesize()](function.getimagesize.md) \- Отримання розміру зображення
-   [imagesx()](function.imagesx.md) \- Отримання ширини зображення
