---
navigation:
  - function.imagechar.md: « imagechar
  - function.imagecolorallocate.md: imagecolorallocate »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecharup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecharup

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecharup — Малювання символу вертикально

### Опис

```methodsynopsis
imagecharup(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $char,    int $color): bool
```

Малює символ `char` вертикально на заданих координатах зображення `image`

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

**Пример #1 Пример использования**imagecharup()\*\*\*\*

```php
<?php

$im = imagecreate(100, 100);

$string = 'Надо учитывать, что первый символ в строке — N';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// печатает чёрный символ "Z" на белом фоне
imagecharup($im, 3, 10, 10, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagecharup()](images/21009b70229598c6a80eef8b45bf282b-imagecharup.png)

### Дивіться також

-   [imagechar()](function.imagechar.md) \- Малювання символу по горизонталі
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
