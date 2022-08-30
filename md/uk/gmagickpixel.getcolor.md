Повертає колір

-   [« GmagickPixel::construct](gmagickpixel.construct.html)
    
-   [GmagickPixel::getcolorcount »](gmagickpixel.getcolorcount.html)
    
-   [PHP Manual](index.html)
    
-   [GmagickPixel](class.gmagickpixel.html)
    
-   Повертає колір
    

# GmagickPixel::getcolor

(PECL gmagick >= Unknown)

GmagickPixel::getcolor — Повертає колір

### Опис

```methodsynopsis
public GmagickPixel::getcolor(bool $as_array = false, bool $normalize_array = false): mixed
```

Повертає колір об'єкту [GmagickPixel](class.gmagickpixel.html) як масиву (array) чи рядки (string). Якщо кольору встановлено прозорість, її значення повертається в четвертому елементі списку.

### Список параметрів

`as_array`

**`true`** для типу повертається значення array, а не string.

`normalize_array`

Значення кольорів буде нормовано, якщо **`true`**

### Значення, що повертаються

string або array зі значеннями кольорів, нормованими, якщо параметр `normalize_array` встановлений в **`true`**. Кидає виняток **GmagickPixelException** у разі виникнення помилки.