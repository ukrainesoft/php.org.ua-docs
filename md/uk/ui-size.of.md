---
navigation:
  - ui-size.getwidth.md: '« UI\\Size::getWidth'
  - ui-size.setheight.md: 'UI\\Size::setHeight »'
  - index.md: PHP Manual
  - class.ui-size.md: UI\\Size
title: 'UI\\Size::of'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Size::of

(UI 1.0.2)

UI\\Size::of — Приведення Point

### Опис

```methodsynopsis
public static UI\Size::of(float $size): UI\Size
```

```methodsynopsis
public static UI\Size::of(UI\Point $point): UI\Size
```

Повинен повернути об'єкт UI\\Size із заданими у вигляді числа з плаваючою комою або у вигляді об'єкта UI\\Point шириною та висотою

### Список параметрів

`size`

Значення для ширини та висоти

`point`

Об'єкт Point для конвертації

### Значення, що повертаються

Об'єкт класу Size
