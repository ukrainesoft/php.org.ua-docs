---
navigation:
  - imagickdraw.getstrokelinecap.md: '« ImagickDraw::getStrokeLineCap'
  - imagickdraw.getstrokemiterlimit.md: 'ImagickDraw::getStrokeMiterLimit »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::getStrokeLineJoin'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::getStrokeLineJoin

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getStrokeLineJoin — Повертає форму, яка буде використовуватися в кутах контурів під час їх обведення

### Опис

```methodsynopsis
public ImagickDraw::getStrokeLineJoin(): int
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Повертає фігуру, яка використовуватиметься в кутах контурів (або інших векторних фігур) під час їх обведення.

### Значення, що повертаються

Повертає одну з констант [LINEJOIN](imagick.constants.md#imagick.constants.linejoin) `imagick::LINEJOIN_*`) або 0, якщо з'єднання лінії обведення не встановлено.
