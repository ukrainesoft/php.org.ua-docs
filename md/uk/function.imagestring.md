---
navigation:
  - function.imagesettile.md: « imagesettile
  - function.imagestringup.md: imagestringup »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagestring
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagestring

(PHP 4, PHP 5, PHP 7, PHP 8)

imagestring — Малювання рядка тексту горизонтально

### Опис

```methodsynopsis
imagestring(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $string,    int $color): bool
```

Малює текст `string` на заданих координатах.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.md), що повертається функцією [imageloadfont()](function.imageloadfont.md) .. .

`x`

x-координата верхнього лівого кута.

`y`

y-координата верхнього лівого кута.

`string`

Рядок тексту.

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

**Пример #1 Пример использования**imagestring()\*\*\*\*

```php
<?php
// Создание изображения 100*30
$im = imagecreate(100, 30);

// Белый фон, синий текст
$bg = imagecolorallocate($im, 255, 255, 255);
$textcolor = imagecolorallocate($im, 0, 0, 255);

// Надпись в левом верхнем углу
imagestring($im, 5, 0, 0, 'Hello world!', $textcolor);

// Вывод изображения
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagestring()](images/21009b70229598c6a80eef8b45bf282b-imagestring.png)

### Дивіться також

-   [imagestringup()](function.imagestringup.md) \- Малювання рядка тексту вертикально
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
-   [imagettftext()](function.imagettftext.md) \- Малювання тексту на зображенні шрифтом TrueType
