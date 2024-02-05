---
navigation:
  - imagick.rotationalblurimage.md: '« Imagick::rotationalBlurImage'
  - imagick.sampleimage.md: 'Imagick::sampleImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::roundCorners'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::roundCorners

(PECL imagick 2, PECL imagick 3)

Imagick::roundCorners — Скруглює кути зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::roundCorners(    float $x_rounding,    float $y_rounding,    float $stroke_width = 10,    float $displace = 5,    float $size_correction = -6): bool
```

Заокруглює кути зображення. Перші два параметри керують ступенем округлення, а останні три параметри можуть використовуватися для точного налаштування процесу округлення. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим. Цей метод недоступний, якщо Imagick був скомпільований з версією ImageMagick 7.0.70 або старшим.

### Список параметрів

`x_rounding`

Округлення по x.

`y_rounding`

Округлення по y.

`stroke_width`

Ширина обведення.

`displace`

Зміщення зображення.

`size_correction`

Корекція розміру.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::roundCorners()\*\*\*\*

Закруглення кутів зображення

```php
<?php

$image = new Imagick();
$image->newPseudoImage(100, 100, "magick:rose");
$image->setImageFormat("png");

$image->roundCorners(5,3);
$image->writeImage("rounded.png");
?>
```
