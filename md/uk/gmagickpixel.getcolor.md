---
navigation:
  - gmagickpixel.construct.md: '« GmagickPixel::construct'
  - gmagickpixel.getcolorcount.md: 'GmagickPixel::getcolorcount »'
  - index.md: PHP Manual
  - class.gmagickpixel.md: GmagickPixel
title: 'GmagickPixel::getcolor'
---
# GmagickPixel::getcolor

(PECL gmagick >= Unknown)

GmagickPixel::getcolor — Повертає колір

### Опис

```methodsynopsis
public GmagickPixel::getcolor(bool $as_array = false, bool $normalize_array = false): mixed
```

Повертає колір об'єкту [GmagickPixel](class.gmagickpixel.md) як масиву (array) чи рядки (string). Якщо кольору встановлено прозорість, її значення повертається в четвертому елементі списку.

### Список параметрів

`as_array`

**`true`** для типу повертається значення array, а не string.

`normalize_array`

Значення кольорів буде нормовано, якщо **`true`**

### Значення, що повертаються

string або array зі значеннями кольорів, нормованими, якщо параметр `normalize_array` встановлений в **`true`**. Кидає виняток **GmagickPixelException** у разі виникнення помилки.
