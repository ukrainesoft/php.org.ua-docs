---
navigation:
  - imagickpixel.getcolorcount.md: '« ImagickPixel::getColorCount'
  - imagickpixel.getcolorvalue.md: 'ImagickPixel::getColorValue »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getColorQuantum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::getColorQuantum

(No version information available, might only be in Git)

ImagickPixel::getColorQuantum — Повертає колір пікселя в масиві у вигляді квантових значень

### Опис

```methodsynopsis
public ImagickPixel::getColorQuantum(): array
```

Повертає колір пікселя у масиві як квантових значень. Якщо ImageMagick був скомпільований як HDRI, це будуть числа з плаваючою точкою, інакше вони будуть цілими числами.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із ключами `"r"` `"g"` `"b"` `"a"`
