Повертає кількість кольорів, пов'язаних з цим кольором

-   [« ImagickPixel::getColorAsString](imagickpixel.getcolorasstring.html)
    
-   [ImagickPixel::getColorQuantum »](imagickpixel.getcolorquantum.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixel](class.imagickpixel.html)
    
-   Повертає кількість кольорів, пов'язаних з цим кольором
    

# ImagickPixel::getColorCount

(PECL imagick 2, PECL imagick 3)

ImagickPixel::getColorCount — Повертає кількість кольорів, пов'язаних із цим кольором.

### Опис

```methodsynopsis
public ImagickPixel::getColorCount(): int
```

Повертає кількість кольорів, пов'язаних із цим кольором.

Кількість пікселів зображення мають той же колір, що і цей ImagickPixel.

ImagickPixel::getColorCount може працювати тільки з об'єктами ImagickPixel, створеними за допомогою Imagick::getImageHistogram()

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає кількість кольорів у вигляді числа, інакше викидає виняток ImagickPixelException.

### Приклади

**Приклад #1 ImagickPixel **getColorCount()****

```php
<?php
    $imagick = new \Imagick();
    $imagick->newPseudoImage(640, 480, "magick:logo");
    $histogramElements = $imagick->getImageHistogram();
    $lastColor = array_pop($histogramElements);
    echo "Last pixel color count is: ".$lastColor->getColorCount();
?>
```

Висновок буде приблизно такий:

```
Last pixel color count is: 256244
```