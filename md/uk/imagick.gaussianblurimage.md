---
navigation:
  - imagick.gammaimage.md: '« Imagick::gammaImage'
  - imagick.getcolorspace.md: 'Imagick::getColorspace »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::gaussianBlurImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::gaussianBlurImage

(PECL imagick 2, PECL imagick 3)

Imagick::gaussianBlurImage — Розмиває зображення

### Опис

```methodsynopsis
public Imagick::gaussianBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Розмиває зображення. Згортає зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (sigma). Для отримання прийнятних результатів radius повинен бути більшим за sigma. При використанні значення radius, що дорівнює 0, метод вибере відповідний радіус.

### Список параметрів

`radius`

Радіус у пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення у пікселях.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::gaussianBlurImage()\*\*\*\*

```php
<?php
function gaussianBlurImage($imagePath, $radius, $sigma, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->gaussianBlurImage($radius, $sigma, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
