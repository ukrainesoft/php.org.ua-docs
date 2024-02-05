---
navigation:
  - imagickdraw.polyline.md: '« ImagickDraw::polyline'
  - imagickdraw.popclippath.md: 'ImagickDraw::popClipPath »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pop

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pop — Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw

### Опис

```methodsynopsis
public ImagickDraw::pop(): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw. Може бути кілька зображень ImagickDraw. Спроба витягти більше зображень ImagickDraw, ніж було додано, призведе до виникнення помилки, правильним використанням є вилучення лише зображень ImagickDraw, які були додані в стек.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
