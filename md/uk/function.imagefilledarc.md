---
navigation:
  - function.imagefill.md: « imagefill
  - function.imagefilledellipse.md: imagefilledellipse »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefilledarc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagefilledarc

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagefilledarc — Малювання та заливання дуги

### Опис

```methodsynopsis
imagefilledarc(    GdImage $image,    int $center_x,    int $center_y,    int $width,    int $height,    int $start_angle,    int $end_angle,    int $color,    int $style): bool
```

Малює дугу з центром у заданих координатах зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`center_x`

x-координат центру.

`center_y`

y-координат центру.

`width`

Ширина дуги.

`height`

Висота дуги.

`start_angle`

Кут початку дуги у градусах.

`end_angle`

Кут закінчення дуги у градусах. 0 ° відповідає положенню 3-години. Дуга малюється за годинниковою стрілкою.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

`style`

Бітова або наступна константа:

1.  **`IMG_ARC_PIE`**
2.  **`IMG_ARC_CHORD`**
3.  **`IMG_ARC_NOFILL`**
4.  **`IMG_ARC_EDGED`**

**`IMG_ARC_PIE`** і **`IMG_ARC_CHORD`** взаємно виключають; **`IMG_ARC_CHORD`** просто з'єднує початок та кінець дуги прямою лінією; **`IMG_ARC_PIE`** малює між ними частину кола . **`IMG_ARC_NOFILL`** означає, що повинні бути тільки межі, заливка не потрібна . **`IMG_ARC_EDGED`**, якщо використовується разом з **`IMG_ARC_NOFILL`**, означає, що початок і кінець дуги з'єднуються з центром - це хороший спосіб (краще заливка) отримати сектор (шматок пирога).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Створення тривимірного пирога**

```php
<?php

// создание изображения
$image = imagecreatetruecolor(100, 100);

// определение цветов
$white    = imagecolorallocate($image, 0xFF, 0xFF, 0xFF);
$gray     = imagecolorallocate($image, 0xC0, 0xC0, 0xC0);
$darkgray = imagecolorallocate($image, 0x90, 0x90, 0x90);
$navy     = imagecolorallocate($image, 0x00, 0x00, 0x80);
$darknavy = imagecolorallocate($image, 0x00, 0x00, 0x50);
$red      = imagecolorallocate($image, 0xFF, 0x00, 0x00);
$darkred  = imagecolorallocate($image, 0x90, 0x00, 0x00);

// делаем эффект 3Д
for ($i = 60; $i > 50; $i--) {
   imagefilledarc($image, 50, $i, 100, 50, 0, 45, $darknavy, IMG_ARC_PIE);
   imagefilledarc($image, 50, $i, 100, 50, 45, 75 , $darkgray, IMG_ARC_PIE);
   imagefilledarc($image, 50, $i, 100, 50, 75, 360 , $darkred, IMG_ARC_PIE);
}

imagefilledarc($image, 50, 50, 100, 50, 0, 45, $navy, IMG_ARC_PIE);
imagefilledarc($image, 50, 50, 100, 50, 45, 75 , $gray, IMG_ARC_PIE);
imagefilledarc($image, 50, 50, 100, 50, 75, 360 , $red, IMG_ARC_PIE);


// вывод изображения
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: Створення тривимірного пирога](images/21009b70229598c6a80eef8b45bf282b-imagefilledarc.png)
