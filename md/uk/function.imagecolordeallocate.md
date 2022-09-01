---
navigation:
  - function.imagecolorclosesthwb.html: « imagecolorclosesthwb
  - function.imagecolorexact.html: imagecolorexact »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagecolordeallocate
---
# imagecolordeallocate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolordeallocate — Розрив асоціації змінної із кольором для заданого зображення

### Опис

```methodsynopsis
imagecolordeallocate(GdImage $image, int $color): bool
```

Розриває асоціацію змінної з кольором, яка раніше була створена функціями [imagecolorallocate()](function.imagecolorallocate.html) або [imagecolorallocatealpha()](function.imagecolorallocatealpha.html)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`color`

Ідентифікатор кольору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolordeallocate()****

```php
<?php
$white = imagecolorallocate($im, 255, 255, 255);
imagecolordeallocate($im, $white);
?>
```

### Дивіться також

-   [imagecolorallocate()](function.imagecolorallocate.html) - Створення кольору для зображення
-   [imagecolorallocatealpha()](function.imagecolorallocatealpha.html) - Створення кольору для зображення
