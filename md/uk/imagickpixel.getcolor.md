Повертає колір

-   [« ImagickPixel::destroy](imagickpixel.destroy.md)
    
-   [ImagickPixel::getColorAsString »](imagickpixel.getcolorasstring.md)
    
-   [PHP Manual](index.md)
    
-   [ImagickPixel](class.imagickpixel.md)
    
-   Повертає колір
    

# ImagickPixel::getColor

(PECL imagick 2, PECL imagick 3)

ImagickPixel::getColor — Повертає колір

### Опис

```methodsynopsis
public ImagickPixel::getColor(int $normalized = 0): array
```

Повертає колір як масив, описаний в об'єкті ImagickPixel. Якщо колір має канал прозорості, він буде відображений у четвертому значенні списку.

### Список параметрів

`normalized`

Нормалізувати значення кольору. Можливі значення: `0` `1` або `2`

**Список можливих значень для `normalized`**

| `normalized` | Описание |
| --- | --- |
| **`0`** | Значення RGB повертаються як цілі числа (int) у діапазоні від `0` до `255` (Включно). Альфа-значення повертається як ціле число (int) і одно або `0`, або `1` |
| **`1`** | Значення RGBA повертаються як числа з плаваючою точкою (float) у діапазоні від `0` до `1` (Включно). |
| **`2`** | Значення RGBA повертаються як цілі числа (int) у діапазоні від `0` до `255` (Включно). |

### Значення, що повертаються

Масив значень каналу. Викидає виняток ImagickPixelException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::getColor()****

```php
<?php

// Создание ImagickPixel со стандартным цветом 'brown'
$color = new ImagickPixel('brown');

// настройка цвета с альфа каналом 25%
$color->setColorValue(Imagick::COLOR_ALPHA, 64 / 256.0);

$colorInfo = $color->getColor();

echo "Стандартные значения" . PHP_EOL;
print_r($colorInfo);

$colorInfo = $color->getColor(1);

echo "Нормализованные значения:" . PHP_EOL;
print_r($colorInfo);

?>
```

Результат виконання цього прикладу:

```
Стандартные значения
Array
(
    [r] => 165
    [g] => 42
    [b] => 42
    [a] => 0
)
Нормализованные значения:
Array
(
    [r] => 0.64705882352941
    [g] => 0.16470588235294
    [b] => 0.16470588235294
    [a] => 0.25000381475547
)
```