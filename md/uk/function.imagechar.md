---
navigation:
  - function.imagebmp.md: « imagebmp
  - function.imagecharup.md: imagecharup »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagechar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagechar

(PHP 4, PHP 5, PHP 7, PHP 8)

imagechar — Малювання символу по горизонталі

### Опис

```methodsynopsis
imagechar(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $char,    int $color): bool
```

**imagechar()** малює перший символ аргументу `char` на зображенні з ідентифікатором `image`на координатах`x`,`y` (координати відраховуються з лівого верхнього кута) кольором `color`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.md), що повертається функцією [imageloadfont()](function.imageloadfont.md) .. .

`x`

x-координата початку малювання.

`y`

y-координата початку малювання.

`char`

Символ для малювання.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`font` тепер приймає як екземпляр [GdFont](class.gdfont.md), і ціле число (int); раніше приймалося лише ціле число (int). |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagechar()\*\*\*\*

```php
<?php

$im = imagecreate(100, 100);

$string = 'PHP';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// печатает чёрный символ "P" в левом верхнем углу
imagechar($im, 1, 0, 0, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagechar()](images/21009b70229598c6a80eef8b45bf282b-imagechar.png)

### Дивіться також

-   [imagecharup()](function.imagecharup.md) \- Малювання символу вертикально
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
