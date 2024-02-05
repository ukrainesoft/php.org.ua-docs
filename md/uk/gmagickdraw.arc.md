---
navigation:
  - gmagickdraw.annotate.md: '« GmagickDraw::annotate'
  - gmagickdraw.bezier.md: 'GmagickDraw::bezier »'
  - index.md: PHP Manual
  - class.gmagickdraw.md: GmagickDraw
title: 'GmagickDraw::arc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GmagickDraw::arc

(PECL gmagick >= Unknown)

GmagickDraw::arc — Малює дугу

### Опис

```methodsynopsis
public GmagickDraw::arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): GmagickDraw
```

Малює дугу, що знаходиться в межах прямокутника, що обмежує, на зображенні.

### Список параметрів

`sx`

Початкова координата x прямокутника, що обмежує.

`sy`

Початкова координата y обмежує прямокутника.

`ex`

Кінцева координата x прямокутника, що обмежує.

`ey`

Кінцева координата y обмежує прямокутника.

`sd`

Початковий градус повороту.

`ed`

Кінцевий градус повороту.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md)
