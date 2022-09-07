---
navigation:
  - function.imageinterlace.md: « imageinterlace
  - function.imagejpeg.md: imagejpeg »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageistruecolor
---
# imageistruecolor

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

imageistruecolor — Визначає, чи зображення є повнокольоровим.

### Опис

```methodsynopsis
imageistruecolor(GdImage $image): bool
```

**imageistruecolor()** визначає, чи є зображення `image` повнокольоровим.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає **`true`**, якщо `image` повнокольорове, **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Просте визначення повнокольорових зображень за допомогою **imageistruecolor()****

```php
<?php
// $im - изображение

// Проверка, является ли изображение полноцветным
if(!imageistruecolor($im))
{
    // Создание truecolor-изображения
    $tc = imagecreatetruecolor(imagesx($im), imagesy($im));

    // копирование из точки
    imagecopy($tc, $im, 0, 0, 0, 0, imagesx($im), imagesy($im));
    imagedestroy($im);

    $im = $tc;
    $tc = NULL;

    // или используйте imagepalettetotruecolor()
}

// Continue working with image instance
?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) - Створення нового повнокольорового зображення
-   [imagepalettetotruecolor()](function.imagepalettetotruecolor.md) - Перетворює зображення на основі палітри на справжній колір
