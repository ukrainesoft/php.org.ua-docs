---
navigation:
  - imagick.setimagescene.md: '« Imagick::setImageScene'
  - imagick.setimagetype.md: 'Imagick::setImageType »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageTicksPerSecond'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageTicksPerSecond

(PECL imagick 2, PECL imagick 3)

Imagick::setImageTicksPerSecond — Встановлює тривалість відображення кадру

### Опис

```methodsynopsis
public Imagick::setImageTicksPerSecond(int $ticks_per_second): bool
```

Регулює тривалість відображення кадру анімованого зображення.

> **Зауваження** :
> 
> Для анімованих GIF-зображень ця функція не змінює кількість "тактів зображення" за секунду, яка завжди визначається як 100. Натомість вона регулює кількість часу, протягом якого відображається кадр, щоб імітувати зміну "тактів за секунду".
> 
> Наприклад, для анімованого GIF-зображення, де кожен кадр відображається протягом 20 тактів (1/5 секунди), коли цей метод викликається для кожного кадру цього зображення з аргументом `50`, кадри коригуються та відображатимуться протягом 40 тактів (2/5 секунди) та анімація відтворюватиметься з половиною вихідної швидкості.

### Список параметрів

`ticks_per_second`

Тривалість, протягом якої має відображатися зображення, виявляється у тактах за секунду.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Зміна анімованого GIF-зображення за допомогою **Imagick::setImageTicksPerSecond()****

```php
<?php

// Изменение анимированного gif-изображения так, чтобы первая половина gif воспроизводилась с половинной скоростью,
// а вторая половина воспроизводилась с удвоенной скоростью.

$imagick = new Imagick(realpath("Test.gif"));
$imagick = $imagick->coalesceImages();

$totalFrames = $imagick->getNumberImages();

$frameCount = 0;

foreach ($imagick as $frame) {
    $imagick->setImageTicksPerSecond(50);

    if ($frameCount < ($totalFrames / 2)) {
        // Измените кадр так, чтобы он отображался вдвое дольше, чем сейчас.
        $imagick->setImageTicksPerSecond(50);
    } else {
        // Измените кадр так, чтобы он отображался вдвое меньше, чем сейчас.
        $imagick->setImageTicksPerSecond(200);
    }

    $frameCount++;
}

$imagick = $imagick->deconstructImages();

$imagick->writeImages("/path/to/save/output.gif", true);

?>
```
