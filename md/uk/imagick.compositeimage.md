---
navigation:
  - imagick.compareimages.md: '« Imagick::compareImages'
  - imagick.construct.md: 'Imagick::construct »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::compositeImage'
---
# Imagick::compositeImage

(PECL imagick 2, PECL imagick 3)

Imagick::compositeImage — Накладає одне зображення на інше

### Опис

```methodsynopsis
public Imagick::compositeImage(    Imagick $composite_object,    int $composite,    int $x,    int $y,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Накладає одне зображення на інше із зазначеним усуненням. Будь-які додаткові аргументи, необхідні для алгоритму накладання, слід передавати в setImageArtifact з 'compose:args' як перший параметр і дані як другий параметр.

### Список параметрів

`composite_object`

Об'єкт Imagick, що містить зображення, що накладається.

`compose`

Оператор накладання. Дивіться [Константи оператора накладання](imagick.constants.html#imagick.constants.compositeop)

`x`

Зміщення стовпця зображення, що накладається.

`y`

Зміщення рядка зображення, що накладається.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::compositeImage()****

Накладання двох зображень за допомогою 'математичного' методу накладання

```php
<?php

// Эквивалентно запуску команды
// convert src1.png src2.png -compose mathematics -define compose:args="1,0,-0.5,0.5" -composite output.png

$src1 = new \Imagick("./src1.png");
$src2 = new \Imagick("./src2.png");

$src1->setImageVirtualPixelMethod(Imagick::VIRTUALPIXELMETHOD_TRANSPARENT);
$src1->setImageArtifact('compose:args', "1,0,-0.5,0.5");
$src1->compositeImage($src2, Imagick::COMPOSITE_MATHEMATICS, 0, 0);
$src1->writeImage("./output.png");

?>
```

### Дивіться також

-   [Imagick::setImageArtifact()](imagick.setimageartifact.md) - Встановлює артефакт зображення
