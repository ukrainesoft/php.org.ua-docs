---
navigation:
  - imagick.setimagebackgroundcolor.html: '« Imagick::setImageBackgroundColor'
  - imagick.setimagebiasquantum.html: 'Imagick::setImageBiasQuantum »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setImageBias'
---
# Imagick::setImageBias

(PECL imagick 2, PECL imagick 3)

Imagick::setImageBias — Встановлює зміщення зображення для будь-якого методу, який згортає зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageBias(float $bias): bool
```

Встановлює зміщення зображення для будь-якого методу, який згортає зображення (наприклад Imagick::ConvolveImage()).

### Список параметрів

`bias`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageBias()****

```php
<?php
//требуется ImageMagick версии 6.9.0-1, чтобы оказывать влияние на convolveImage
function setImageBias($bias) {
    $imagick = new \Imagick(realpath("images/stack.jpg"));

    $xKernel = array(
        -0.70, 0, 0.70,
        -0.70, 0, 0.70,
        -0.70, 0, 0.70
    );

    $imagick->setImageBias($bias * \Imagick::getQuantum());
    $imagick->convolveImage($xKernel, \Imagick::CHANNEL_ALL);

    $imagick->setImageFormat('png');

    header('Content-type: image/png');
    echo $imagick->getImageBlob();
}

?>
```
