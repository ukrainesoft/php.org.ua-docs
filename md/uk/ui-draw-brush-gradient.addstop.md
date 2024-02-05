---
navigation:
  - class.ui-draw-brush-gradient.md: « UI\\Draw\\Brush\\Gradient
  - ui-draw-brush-gradient.delstop.md: 'UI\\Draw\\Brush\\Gradient::delStop »'
  - index.md: PHP Manual
  - class.ui-draw-brush-gradient.md: UI\\Draw\\Brush\\Gradient
title: 'UI\\Draw\\Brush\\Gradient::addStop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Draw\\Brush\\Gradient::addStop

(UI 2.0.0)

UI\\Draw\\Brush\\Gradient::addStop — Додає вузол градієнта

### Опис

```methodsynopsis
public UI\Draw\Brush\Gradient::addStop(float $position, UI\Draw\Color $color): int
```

```methodsynopsis
public UI\Draw\Brush\Gradient::addStop(float $position, int $color): int
```

Додає вузол градієнта заданого кольору заданої позиції.

### Список параметрів

`position`

Позиція нового вузла.

`color`

Колір для нового вузла, можливо UI\\Draw\\Color або RRGGBBAA.

### Значення, що повертаються

Загальна кількість вузлів.
