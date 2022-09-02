---
navigation:
  - imagickdraw.getfontstretch.md: '« ImagickDraw::getFontStretch'
  - imagickdraw.getfontweight.md: 'ImagickDraw::getFontWeight »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::getFontStyle'
---
# ImagickDraw::getFontStyle

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getFontStyle — Повертає стиль шрифту

### Опис

```methodsynopsis
public ImagickDraw::getFontStyle(): int
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає стиль шрифту, який використовується під час анотації тексту.

### Значення, що повертаються

Повертає константу [STYLE](imagick.constants.md#imagick.constants.styles) `imagick::STYLE_*`), пов'язану з об'єктом [ImagickDraw](class.imagickdraw.md) або 0, якщо стиль не встановлено.
