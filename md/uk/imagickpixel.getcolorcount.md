---
navigation:
  - imagickpixel.getcolorasstring.md: '« ImagickPixel::getColorAsString'
  - imagickpixel.getcolorquantum.md: 'ImagickPixel::getColorQuantum »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getColorCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::getColorCount

(PECL imagick 2, PECL imagick 3)

ImagickPixel::getColorCount — Повертає кількість кольорів, пов'язаних із цим кольором.

### Опис

```methodsynopsis
public ImagickPixel::getColorCount(): int
```

Повертає кількість кольорів, пов'язаних із цим кольором.

Кількість пікселів зображення має той же колір, що і цей ImagickPixel.

ImagickPixel::getColorCount може працювати тільки з об'єктами ImagickPixel, створеними за допомогою Imagick::getImageHistogram()

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає кількість кольорів у вигляді числа, інакше викидає виняток ImagickPixelException.

### Приклади

**Пример #1 ImagickPixel**getColorCount()\*\*\*\*

```php
<?php
    $imagick = new \Imagick();
    $imagick->newPseudoImage(640, 480, "magick:logo");
    $histogramElements = $imagick->getImageHistogram();
    $lastColor = array_pop($histogramElements);
    echo "Last pixel color count is: ".$lastColor->getColorCount();
?>
```

Висновок буде приблизно такий:

```
Last pixel color count is: 256244
```
