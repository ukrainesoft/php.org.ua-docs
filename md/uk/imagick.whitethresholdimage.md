---
navigation:
  - imagick.waveimage.md: '« Imagick::waveImage'
  - imagick.writeimage.md: 'Imagick::writeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::whiteThresholdImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::whiteThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::whiteThresholdImage — Зафарбовує всі пікселі вище за поріг у білий

### Опис

```methodsynopsis
public Imagick::whiteThresholdImage(mixed $threshold): bool
```

Схожий на Imagick::ThresholdImage(), але зафарбовує всі пікселі вище за поріг у білий колір, залишаючи всі пікселі нижче порога без змін.

### Список параметрів

`threshold`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяється передавати рядок, який представляє колір як параметр. Попередні версії допускають лише об'єкт ImagickPixel. |

### Приклади

**Пример #1 Пример использования**Imagick::whiteThresholdImage()\*\*\*\*

```php
<?php
function whiteThresholdImage($imagePath, $color) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->whiteThresholdImage($color);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
