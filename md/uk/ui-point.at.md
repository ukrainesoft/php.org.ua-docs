---
navigation:
  - class.ui-point.html: « UIPoint
  - ui-point.construct.html: 'ОЙPoint::construct »'
  - index.md: PHP Manual
  - class.ui-point.html: ОЙPoint
title: 'ОЙPoint::at'
---
# ОЙPoint::at

(UI 1.0.2)

ОЙPoint::at — Приведення Size

### Опис

```methodsynopsis
public static UI\Point::at(float $point): UI\Point
```

```methodsynopsis
public static UI\Point::at(UI\Size $size): UI\Point
```

Повинен повернути об'єкт UIPoint з координатами x і y, заданими у вигляді числа з точкою, що плаває, або у вигляді об'єкта UISize.

### Список параметрів

`point`

Значення для x та y

`size`

Об'єкт класу Size для конвертації

### Значення, що повертаються

Об'єкт класу Point
