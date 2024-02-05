---
navigation:
  - imagick.appendimages.md: '« Imagick::appendImages'
  - imagick.averageimages.md: 'Imagick::averageImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::autoLevelImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::autoLevelImage

(PECL imagick 3 >= 3.3.0)

Imagick::autoLevelImage — Налаштовує рівні певного каналу зображення

### Опис

```methodsynopsis
public Imagick::autoLevelImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Налаштовує рівні певного каналу зображення, масштабуючи мінімальне та максимальне значення до повного квантового діапазону.

### Список параметрів

`channel`

На якому каналі слід здійснити автоматичне вирівнювання.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::autoLevelImage()\*\*\*\*

```php
<?php
function autoLevelImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->autoLevelImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
