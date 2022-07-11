- [« Imagick::setImageBackgroundColor](imagick.setimagebackgroundcolor.md)
- [Imagick::setImageBiasQuantum »](imagick.setimagebiasquantum.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Встановлює зміщення зображення для будь-якого методу, який
згортає зображення

# Imagick::setImageBias

(PECL imagick 2, PECL imagick 3)

Imagick::setImageBias — Встановлює зміщення зображення для кожного
методу, який згортає зображення

**Увага**

Функція оголошена *УСТАРШЕНОЮ* в Imagick 3.4.4. Покладатись на цю
функцію не рекомендується.

### Опис

public **Imagick::setImageBias**(float `$bias`): bool

Встановлює зміщення зображення для будь-якого методу, який згортає
зображення (наприклад, Imagick::ConvolveImage()).

### Список параметрів

`bias`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageBias()****

` <?php//потрібна ImageMagick версії 6.9.0-1, надавати вплив на convolveImagefunction setImageBias($bias) {    $imagick = new \Imagick(real) $xKernel==array(-0.70,0,7,0,7,0,7,0,7,0,7,0,7,0,7,0,7,0,7,0,7-0,7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0.7-0. $imagick->setImageBias($bias * \Imagick::getQuantum()); $imagick->convolveImage($xKernel, \Imagick::CHANNEL_ALL); $imagick->setImageFormat('png'); header('Content-type: image/png'); echo $imagick->getImageBlob();}?> `
