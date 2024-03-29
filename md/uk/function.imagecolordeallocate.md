---
navigation:
  - function.imagecolorclosesthwb.md: « imagecolorclosesthwb
  - function.imagecolorexact.md: imagecolorexact »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolordeallocate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolordeallocate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolordeallocate — Розрив асоціації змінної із кольором для заданого зображення

### Опис

```methodsynopsis
imagecolordeallocate(GdImage $image, int $color): bool
```

Розриває асоціацію змінної з кольором, яка раніше була створена функціями [imagecolorallocate()](function.imagecolorallocate.md) або [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`color`

Ідентифікатор кольору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagecolordeallocate()\*\*\*\*

```php
<?php
$white = imagecolorallocate($im, 255, 255, 255);
imagecolordeallocate($im, $white);
?>
```

### Дивіться також

-   [imagecolorallocate()](function.imagecolorallocate.md) \- Створення кольору для зображення
-   [imagecolorallocatealpha()](function.imagecolorallocatealpha.md) \- Створення кольору для зображення
