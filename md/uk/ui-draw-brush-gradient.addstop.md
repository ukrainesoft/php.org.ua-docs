---
navigation:
  - class.ui-draw-brush-gradient.md: « UIDrawBrushGradient
  - ui-draw-brush-gradient.delstop.md: 'ОЙDrawBrushGradient::delStop »'
  - index.md: PHP Manual
  - class.ui-draw-brush-gradient.md: ОЙDrawBrushGradient
title: 'ОЙDrawBrushGradient::addStop'
---
# ОЙDrawBrushGradient::addStop

(UI 2.0.0)

ОЙDrawBrushGradient::addStop — Додає вузол градієнта

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

Колір для нового вузла, можливо UIDrawColor або RRGGBBAA.

### Значення, що повертаються

Загальна кількість вузлів.
