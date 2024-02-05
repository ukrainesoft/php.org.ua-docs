---
navigation:
  - imagick.shaveimage.md: '« Imagick::shaveImage'
  - imagick.sigmoidalcontrastimage.md: 'Imagick::sigmoidalContrastImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::shearImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::shearImage

(PECL imagick 2, PECL imagick 3)

Imagick::shearImage — Створює паралелограм

### Опис

```methodsynopsis
public Imagick::shearImage(mixed $background, float $x_shear, float $y_shear): bool
```

Зсуває один край зображення по осі X або Y, утворюючи паралелограм. Зсув в напрямку X зсуває край осі X, а зсув в напрямку Y переміщує край осі Y. Величина зсуву контролюється кутом зсуву. Для зсуву у напрямку X, x\_shear вимірюється щодо осі Y та аналогічно для зсуву в напрямку Y, y\_shear вимірюється щодо осі X. Порожні трикутники, що залишилися від обрізки зображення, заповнюються кольором тла.

### Список параметрів

`background`

Колір фону.

`x_shear`

Кількість градусів для зсуву осі X.

`y_shear`

Кількість градусів для зсуву осі Y.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер допускається рядок, що представляє колір, як перший параметр. Раніше допускався лише об'єкт ImagickPixel. |

### Приклади

**Пример #1 Пример использования**Imagick::shearImage()\*\*\*\*

```php
<?php
function shearImage($imagePath, $color, $shearX, $shearY) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->shearimage($color, $shearX, $shearY);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
