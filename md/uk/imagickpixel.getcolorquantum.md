---
navigation:
  - imagickpixel.getcolorcount.md: '« ImagickPixel::getColorCount'
  - imagickpixel.getcolorvalue.md: 'ImagickPixel::getColorValue »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getColorQuantum'
---
# ImagickPixel::getColorQuantum

(No version information available, might only be in Git)

ImagickPixel::getColorQuantum — Опис

### Опис

```methodsynopsis
public ImagickPixel::getColorQuantum(): array
```

Повертає колір пікселя у масиві як квантових значень. Якщо ImageMagick був скомпільований як HDRI, це будуть числа з плаваючою точкою, інакше вони будуть цілими числами.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із ключами `"r"` `"g"` `"b"` `"a"`
