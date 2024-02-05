---
navigation:
  - function.imagesetpixel.md: « imagesetpixel
  - function.imagesetthickness.md: imagesetthickness »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesetstyle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagesetstyle

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagesetstyle — Налаштування стилю малювання ліній

### Опис

```methodsynopsis
imagesetstyle(GdImage $image, array $style): bool
```

**imagesetstyle()** задає стиль, який використовуватиметься функціями малювання ліній (такими як [imageline()](function.imageline.md) і [imagepolygon()](function.imagepolygon.md)) при задании специального цвета\*\*`IMG_COLOR_STYLED`** або **`IMG_COLOR_STYLEDBRUSHED`\*\*

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`style`

Масив з квітами пікселів. Можна використовувати константу \*\*`IMG_COLOR_TRANSPARENT`\*\*для добавления прозрачной точки. Обратите внимание, что`style` не має бути порожнім масивом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Наступний приклад малює пунктирну лінію з лівого верхнього кута зображення в нижній правий:

**Приклад #1 Приклад використання** imagesetstyle()\*\*\*\*

```php
<?php
header("Content-type: image/jpeg");
$im  = imagecreatetruecolor(100, 100);
$w   = imagecolorallocate($im, 255, 255, 255);
$red = imagecolorallocate($im, 255, 0, 0);

/* Рисование пунктирной линии, 5 красных точек, 5 белых */
$style = array($red, $red, $red, $red, $red, $w, $w, $w, $w, $w);
imagesetstyle($im, $style);
imageline($im, 0, 0, 100, 100, IMG_COLOR_STYLED);

/* Рисование линии из смайликов, используя imagesetbrush() с imagesetstyle */
$style = array($w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $red);
imagesetstyle($im, $style);

$brush = imagecreatefrompng("http://www.libpng.org/pub/png/images/smile.happy.png");
$w2 = imagecolorallocate($brush, 255, 255, 255);
imagecolortransparent($brush, $w2);
imagesetbrush($im, $brush);
imageline($im, 100, 0, 0, 100, IMG_COLOR_STYLEDBRUSHED);

imagejpeg($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagesetstyle()](images/21009b70229598c6a80eef8b45bf282b-imagesetstyle.jpg)

### Дивіться також

-   [imagesetbrush()](function.imagesetbrush.md) \- Встановлення зображення (пензля), за допомогою якого будуть малюватись лінії
-   [imageline()](function.imageline.md) \- Малювання лінії
