---
navigation:
  - imagick.importimagepixels.md: '« Imagick::importImagePixels'
  - imagick.labelimage.md: 'Imagick::labelImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::inverseFourierTransformImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::inverseFourierTransformImage

(PECL imagick 3 >= 3.3.0)

Imagick::inverseFourierTransformImage — Реалізує дискретне перетворення Фур'є

### Опис

```methodsynopsis
public Imagick::inverseFourierTransformImage(Imagick $complement, bool $magnitude): bool
```

Реалізує дискретне перетворення Фур'є (ДПФ) зображення у вигляді пари величина/фаза або пари, що складається з реального/уявного зображень.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`complement`

Друге зображення, яке потрібно об'єднати з даними, щоб сформувати або пару величина/фаза, або пару з реального/уявного зображень.

`magnitude`

Якщо значення дорівнює true, буде повернуто пару величина/фаза, інакше – пара, що складається з реального/уявного зображень.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
