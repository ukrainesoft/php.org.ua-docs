---
navigation:
  - function.imagestring.md: « imagestring
  - function.imagesx.md: imagesx »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagestringup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagestringup

(PHP 4, PHP 5, PHP 7, PHP 8)

imagestringup — Малювання рядка тексту вертикально

### Опис

```methodsynopsis
imagestringup(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $string,    int $color): bool
```

Малює текст `string` вертикально на заданих координатах.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.md), що повертається функцією [imageloadfont()](function.imageloadfont.md) .. .

`x`

x-координата нижнього лівого кута.

`y`

y-координата нижнього лівого кута.

`string`

Текст написи.

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

**Приклад #1 Приклад використання** imagestringup()\*\*\*\*

```php
<?php
// Создание изображения 100*100
$im = imagecreatetruecolor(100, 100);

// Надпись
$textcolor = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
imagestringup($im, 3, 40, 80, 'gd library', $textcolor);

// Сохранение изображения
imagepng($im, './stringup.png');
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagestringup()](images/21009b70229598c6a80eef8b45bf282b-imagestringup.png)

### Дивіться також

-   [imagestring()](function.imagestring.md) \- Малювання рядка тексту горизонтально
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
