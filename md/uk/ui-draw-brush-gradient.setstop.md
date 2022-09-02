---
navigation:
  - ui-draw-brush-gradient.delstop.md: '« UIDrawBrushGradient::delStop'
  - class.ui-draw-brush-lineargradient.md: ОЙDrawBrushLinearGradient »
  - index.md: PHP Manual
  - class.ui-draw-brush-gradient.md: ОЙDrawBrushGradient
title: 'ОЙDrawBrushGradient::setStop'
---
# ОЙDrawBrushGradient::setStop

(UI 2.0.0)

ОЙDrawBrushGradient::SetStop - Встановлює вузол градієнта

### Опис

```methodsynopsis
public UI\Draw\Brush\Gradient::setStop(int $index, float $position, UI\Draw\Color $color): bool
```

```methodsynopsis
public UI\Draw\Brush\Gradient::setStop(int $index, float $position, int $color): bool
```

### Список параметрів

`index`

Індекс вузла для встановлення.

`position`

Позиція для сайту.

`color`

Колір для нового вузла, можливо UIDrawColor або RRGGBBAA.

### Значення, що повертаються

Індикація успіху.
