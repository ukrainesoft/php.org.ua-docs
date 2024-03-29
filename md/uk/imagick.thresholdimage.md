---
navigation:
  - imagick.textureimage.md: '« Imagick::textureImage'
  - imagick.thumbnailimage.md: 'Imagick::thumbnailImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::thresholdImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::thresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::thresholdImage — Змінює окремі пікселі на основі порогового значення

### Опис

```methodsynopsis
public Imagick::thresholdImage(float $threshold, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює окремі пікселі залежно від їхньої інтенсивності в порівнянні з пороговим значенням. Результатом буде високо-контрастне, двоколірне зображення.

### Список параметрів

`threshold`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::thresholdImage()\*\*\*\*

```php
<?php
function thresholdimage($imagePath, $threshold, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->thresholdimage($threshold * \Imagick::getQuantum(), $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
