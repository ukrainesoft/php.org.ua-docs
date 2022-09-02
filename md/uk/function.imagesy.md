---
navigation:
  - function.imagesx.md: « imagesx
  - function.imagetruecolortopalette.md: imagetruecolortopalette »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesy
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

Повертає висоту зображення `image` або **`false`** у разі помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesy()****

```php
<?php

// Создание изображения 300*200
$img = imagecreatetruecolor(300, 200);

echo imagesy($img); // 200

?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) - Створення нового повнокольорового зображення
-   [getimagesize()](function.getimagesize.md) - Отримання розміру зображення
-   [imagesx()](function.imagesx.md) - Отримання ширини зображення
