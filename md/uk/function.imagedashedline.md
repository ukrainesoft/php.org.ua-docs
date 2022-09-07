---
navigation:
  - function.imagecropauto.md: « imagecropauto
  - function.imagedestroy.md: imagedestroy »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagedashedline
---
# imagedashedline

(PHP 4, PHP 5, PHP 7, PHP 8)

imagedashedline — Малювання пунктирної лінії

### Опис

```methodsynopsis
imagedashedline(    GdImage $image,    int $x1,    int $y1,    int $x2,    int $y2,    int $color): bool
```

Функція застаріла. Використовуйте поєднання функцій [imagesetstyle()](function.imagesetstyle.md) і [imageline()](function.imageline.md)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x1`

Верхня ліва x-координата.

`y1`

Верхня ліва y-координата. 0, 0 – верхній лівий кут зображення.

`x2`

Нижня права х-координата.

`y2`

Нижня права у-координата.

`color`

Колір лінії. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagedashedline()****

```php
<?php
// Создание изображения 100x100
$im = imagecreatetruecolor(100, 100);
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);

// Рисование вертикальной пунктирной линии
imagedashedline($im, 50, 25, 50, 75, $white);

// Сохранение изображения
imagepng($im, './dashedline.png');
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagedashedline()](images/21009b70229598c6a80eef8b45bf282b-imagedashedline.png)

**Приклад #2 Альтернатива функції **imagedashedline()****

```php
<?php
// Создание изображения 100x100
$im = imagecreatetruecolor(100, 100);
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);

// Определение стиля: Первые 4 пиксела белые, следующие 4 - прозрачные.
// Это создаёт эффект пунктира.
$style = Array(
                $white,
                $white,
                $white,
                $white,
                IMG_COLOR_TRANSPARENT,
                IMG_COLOR_TRANSPARENT,
                IMG_COLOR_TRANSPARENT,
                IMG_COLOR_TRANSPARENT
                );

imagesetstyle($im, $style);

// Рисование пунктирной линии
imageline($im, 50, 25, 50, 75, IMG_COLOR_STYLED);

// Сохранение изображения
imagepng($im, './imageline.png');
imagedestroy($im);
?>
```

### Дивіться також

-   [imagesetstyle()](function.imagesetstyle.md) - Встановлення стилю малювання ліній
-   [imageline()](function.imageline.md) - Малювання лінії
