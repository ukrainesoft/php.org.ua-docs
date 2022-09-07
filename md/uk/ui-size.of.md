---
navigation:
  - ui-size.getwidth.md: '« UISize::getWidth'
  - ui-size.setheight.md: 'ОЙSize::setHeight »'
  - index.md: PHP Manual
  - class.ui-size.md: ОЙSize
title: 'ОЙSize::of'
---
# ОЙSize::of

(UI 1.0.2)

ОЙSize::of — Приведення Point

### Опис

```methodsynopsis
public static UI\Size::of(float $size): UI\Size
```

```methodsynopsis
public static UI\Size::of(UI\Point $point): UI\Size
```

Повинен повернути об'єкт UISize із заданими у вигляді числа з плаваючою комою або у вигляді об'єкта UIPoint шириною та висотою

### Список параметрів

`size`

Значення для ширини та висоти

`point`

Об'єкт Point для конвертації

### Значення, що повертаються

Об'єкт класу Size
