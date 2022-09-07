---
navigation:
  - imagickpixel.getcolor.md: '« ImagickPixel::getColor'
  - imagickpixel.getcolorcount.md: 'ImagickPixel::getColorCount »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getColorAsString'
---
# ImagickPixel::getColorAsString

(PECL imagick 2> = 2.1.0, PECL imagick 3)

ImagickPixel::getColorAsString — Повертає колір у вигляді рядка

### Опис

```methodsynopsis
public ImagickPixel::getColorAsString(): string
```

Повертає колір об'єкта ImagickPixel у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає колір об'єкта ImagickPixel у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **Imagick::getColorAsString()****

```php
<?php

// Создание ImagickPixel со стандартным цветом 'brown'
$color = new ImagickPixel('brown');

$color->setColorValue(Imagick::COLOR_ALPHA, 64 / 256.0);

$colorInfo = $color->getColorAsString();

print_r($colorInfo);
?>
```

Результат виконання цього прикладу:

```
rgb(165,42,42)
```

### Примітки

> **Зауваження** **Альфа канал не повертається**
> 
> Функція не повертає значення альфа-каналу для кольору.
