---
navigation:
  - function.imagebmp.html: « imagebmp
  - function.imagecharup.html: imagecharup »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagechar
---
# imagechar

(PHP 4, PHP 5, PHP 7, PHP 8)

imagechar — Малювання символу по горизонталі

### Опис

```methodsynopsis
imagechar(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $char,    int $color): bool
```

**imagechar()** малює перший символ аргументу `char` на зображенні з ідентифікатором `image` на координатах `x``y` (координати відраховуються з лівого верхнього кута) кольором `color`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

`x`

x-координата початку малювання.

`y`

y-координата початку малювання.

`char`

Символ для малювання.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `font` тепер приймає як екземпляр [GdFont](class.gdfont.html), і ціле число (int); раніше приймалося лише ціле число (int). |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagechar()****

```php
<?php

$im = imagecreate(100, 100);

$string = 'PHP';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// печатает чёрный символ "P" в левом верхнем углу
imagechar($im, 1, 0, 0, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagechar()](images/21009b70229598c6a80eef8b45bf282b-imagechar.png)

### Дивіться також

-   [imagecharup()](function.imagecharup.html) - Малювання символу вертикально
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту
