---
navigation:
  - imagick.averageimages.md: '« Imagick::averageImages'
  - imagick.blueshiftimage.md: 'Imagick::blueShiftImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::blackThresholdImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::blackThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::blackThresholdImage — Перекласти всі пікселі нижче граничного значення в чорний колір

### Опис

```methodsynopsis
public Imagick::blackThresholdImage(mixed $threshold): bool
```

Працює так само, як Imagick::thresholdImage(), але змінюються тільки пікселі нижче порогового значення, тоді як інші пікселі залишаються незмінними.

### Список параметрів

`threshold`

Порогове значення нижче якого всі пікселі стануть чорними

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Як параметр можна передавати колір рядком. У попередніх версіях дозволялося передавати лише ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання** Imagick::blackThresholdImage()\*\*\*\*

```php
<?php
function blackThresholdImage($imagePath, $thresholdColor) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->blackthresholdimage($thresholdColor);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
