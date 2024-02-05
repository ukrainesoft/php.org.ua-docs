---
navigation:
  - class.ui-point.md: « UI\\Point
  - ui-point.construct.md: 'UI\\Point::\_\_construct »'
  - index.md: PHP Manual
  - class.ui-point.md: UI\\Point
title: 'UI\\Point::at'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Point::at

(UI 1.0.2)

UI\\Point::at — Приведення Size

### Опис

```methodsynopsis
public static UI\Point::at(float $point): UI\Point
```

```methodsynopsis
public static UI\Point::at(UI\Size $size): UI\Point
```

Повинен повернути об'єкт UI\\Point з координатами x і y, заданими у вигляді числа з точкою, що плаває, або у вигляді об'єкта UI\\Size.

### Список параметрів

`point`

Значення для x та y

`size`

Об'єкт класу Size для конвертації

### Значення, що повертаються

Об'єкт класу Point
