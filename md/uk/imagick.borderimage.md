---
navigation:
  - imagick.blurimage.html: '« Imagick::blurImage'
  - imagick.brightnesscontrastimage.html: 'Imagick::brightnessContrastImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::borderImage'
---
# Imagick::borderImage

(PECL imagick 2, PECL imagick 3)

Imagick::borderImage — Оточує зображення рамкою

### Опис

```methodsynopsis
public Imagick::borderImage(mixed $bordercolor, int $width, int $height): bool
```

Оточує зображення рамкою із кольором, встановленим в об'єкті ImagickPixel.

### Список параметрів

`bordercolor`

Об'єкт ImagickPixel або рядок, що містить колір рамки

`width`

Ширина рамки

`height`

Висота рамки

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Як колір можна передавати рядок. Попередні версії допускали лише об'єкт ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання **Imagick::borderImage()****

```php
<?php
function borderImage($imagePath, $color, $width, $height) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->borderImage($color, $width, $height);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
