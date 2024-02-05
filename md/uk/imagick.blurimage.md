---
navigation:
  - imagick.blueshiftimage.md: '« Imagick::blueShiftImage'
  - imagick.borderimage.md: 'Imagick::borderImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::blurImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::blurImage

(PECL imagick 2, PECL imagick 3)

Imagick::blurImage — Додає фільтр розмиття до зображення

### Опис

```methodsynopsis
public Imagick::blurImage(float $radius, float $sigma, int $channel = ?): bool
```

Додає фільтр розмиття до зображення. Необов'язковий третій параметр використовується для розмиття певного каналу.

### Список параметрів

`radius`

Радіус розмиття

`sigma`

Стандартне відхилення

`channel`

Константа[Channeltype](imagick.constants.md#imagick.constants.channel). Якщо не вказано, будуть розмиті всі канали.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::blurImage()\*\* :\*\*

Розмиття зображення та надсилання його до браузера.

```php
<?php

header('Content-type: image/jpeg');

$image = new Imagick('test.jpg');

$image->blurImage(5,3);
echo $image;

?>
```

### Дивіться також

-   [Imagick::adaptiveBlurImage()](imagick.adaptiveblurimage.md) \- Додає адаптивний фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.md) \- Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.md) \- Радіальне розмиття зображення
