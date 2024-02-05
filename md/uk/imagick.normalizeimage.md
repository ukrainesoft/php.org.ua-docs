---
navigation:
  - imagick.nextimage.md: '« Imagick::nextImage'
  - imagick.oilpaintimage.md: 'Imagick::oilPaintImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::normalizeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::normalizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::normalizeImage — Підвищує контрастність кольорового зображення

### Опис

```methodsynopsis
public Imagick::normalizeImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Підвищує контраст кольорового зображення, регулюючи колір пікселів для охоплення всього діапазону доступних кольорів.

### Список параметрів

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для заданого режиму каналу. Для застосування більш ніж одного каналу необхідно об'єднати константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::normalizeImage()\*\*\*\*

```php
<?php
function normalizeImage($imagePath, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $original = clone $imagick;
    $original->cropimage($original->getImageWidth() / 2, $original->getImageHeight(), 0, 0);
    $imagick->normalizeImage($channel);
    $imagick->compositeimage($original, \Imagick::COMPOSITE_ATOP, 0, 0);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
