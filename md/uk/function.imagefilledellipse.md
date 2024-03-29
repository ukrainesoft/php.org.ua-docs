---
navigation:
  - function.imagefilledarc.md: « imagefilledarc
  - function.imagefilledpolygon.md: imagefilledpolygon »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefilledellipse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagefilledellipse

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagefilledellipse - Малювання зафарбованого еліпса

### Опис

```methodsynopsis
imagefilledellipse(    GdImage $image,    int $center_x,    int $center_y,    int $width,    int $height,    int $color): bool
```

Малює еліпс із центром у заданих координатах зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`center_x`

x-координат центру.

`center_y`

y-координат центру.

`width`

Ширина еліпса.

`height`

Висота еліпса.

`color`

Колір заливки. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagefilledellipse()\*\*\*\*

```php
<?php

// создание пустого изображения
$image = imagecreatetruecolor(400, 300);

// заливка фона
$bg = imagecolorallocate($image, 0, 0, 0);

// выбор цвета для эллипса
$col_ellipse = imagecolorallocate($image, 255, 255, 255);

// рисование белого эллипса
imagefilledellipse($image, 200, 150, 300, 200, $col_ellipse);

// вывод картинки
header("Content-type: image/png");
imagepng($image);

?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagefilledellipse()](images/21009b70229598c6a80eef8b45bf282b-imagefilledellipse.png)

### Примітки

> **Зауваження** :
> 
> **imagefilledellipse()** ігнорує [imagesetthickness()](function.imagesetthickness.md)

### Дивіться також

-   [imageellipse()](function.imageellipse.md) \- Малювання еліпса
-   [imagefilledarc()](function.imagefilledarc.md) \- Малювання та заливання дуги
