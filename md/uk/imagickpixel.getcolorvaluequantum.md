Опис

-   [« ImagickPixel::getColorValue](imagickpixel.getcolorvalue.html)
    
-   [ImagickPixel::getHSL »](imagickpixel.gethsl.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixel](class.imagickpixel.html)
    
-   Опис
    

# ImagickPixel::getColorValueQuantum

(PECL imagick 2> = 2.3.0, PECL imagick 3)

ImagickPixel::getColorValueQuantum — Опис

### Опис

```methodsynopsis
public ImagickPixel::getColorValueQuantum(int $color): int|float
```

Отримує квантове значення кольору ImagickPixel. Значення, що повертається - це число з плаваючою точкою, якщо ImageMagick був скомпільований з HDRI, в іншому випадку - ціле число.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Квантове значення кольору. Число з плаваючою точкою, якщо ImageMagick був скомпільований з HDRI, інакше ціле число.

### Приклади

**Приклад #1 Приклад використання **ImagickPixel::getColorValueQuantum()****

```php
<?php
        $color = new \ImagickPixel('rgb(128, 5, 255)');
        $colorRed = $color->getColorValueQuantum(\Imagick::COLOR_RED);
        $colorGreen = $color->getColorValueQuantum(\Imagick::COLOR_GREEN);
        $colorBlue = $color->getColorValueQuantum(\Imagick::COLOR_BLUE);
        $colorAlpha = $color->getColorValueQuantum(\Imagick::COLOR_ALPHA);

        printf(
            "Красный: %s Зелёный: %s  Синий %s Альфа: %s",
            $colorRed,
            $colorGreen,
            $colorBlue,
            $colorAlpha
        );

?>
```