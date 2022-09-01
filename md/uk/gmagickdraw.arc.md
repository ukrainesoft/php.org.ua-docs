---
navigation:
  - gmagickdraw.annotate.html: '« GmagickDraw::annotate'
  - gmagickdraw.bezier.html: 'GmagickDraw::bezier »'
  - index.html: PHP Manual
  - class.gmagickdraw.html: GmagickDraw
title: 'GmagickDraw::arc'
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

Об'єкт [Gmagick](class.gmagick.html)
