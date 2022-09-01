---
navigation:
  - imagickdraw.getstrokedashoffset.md: '« ImagickDraw::getStrokeDashOffset'
  - imagickdraw.getstrokelinejoin.md: 'ImagickDraw::getStrokeLineJoin »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::getStrokeLineCap'
---
# ImagickDraw::getStrokeLineCap

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getStrokeLineCap — Повертає форму, яка буде використовуватися в кінці відкритих внутрішніх контурів під час їх обведення

### Опис

```methodsynopsis
public ImagickDraw::getStrokeLineCap(): int
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення.

### Значення, що повертаються

Повертає константу [LINECAP](imagick.constants.html#imagick.constants.linecap) `imagick::LINECAP_*`) або 0, якщо форма обведення не задана.
