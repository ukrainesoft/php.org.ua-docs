---
navigation:
  - imagick.functionimage.md: '« Imagick::functionImage'
  - imagick.gammaimage.md: 'Imagick::gammaImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::fxImage'
---
# Imagick::fxImage

(PECL imagick 2, PECL imagick 3)

Imagick::fxImage — Оцінює вираз для кожного пікселя у зображенні

### Опис

```methodsynopsis
public Imagick::fxImage(string $expression, int $channel = Imagick::CHANNEL_DEFAULT): Imagick
```

Оцінює вираз для кожного пікселя у зображенні. Подивіться докладніше про [» Оператор зображення Fx зі спеціальними ефектами](http://www.imagemagick.org/script/fx.php) для отримання додаткової інформації.

### Список параметрів

`expression`

Вираз

`channel`

Вкажіть будь-яку постійну каналу, яка підходить для режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу, використовуючи побітові оператори. Перегляньте цей список [констант канала](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::fxImage()****

```php
<?php
function fxImage() {
    $imagick = new \Imagick();
    $imagick->newPseudoImage(200, 200, "xc:white");

    $fx = 'xx=i-w/2; yy=j-h/2; rr=hypot(xx,yy); (.5-rr/140)*1.2+.5';
    $fxImage = $imagick->fxImage($fx);

    header("Content-Type: image/png");
    $fxImage->setimageformat('png');
    echo $fxImage->getImageBlob();
}

?>
```
