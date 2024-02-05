---
navigation:
  - ui-draw-brush-gradient.delstop.md: '« UI\\Draw\\Brush\\Gradient::delStop'
  - class.ui-draw-brush-lineargradient.md: UI\\Draw\\Brush\\LinearGradient »
  - index.md: PHP Manual
  - class.ui-draw-brush-gradient.md: UI\\Draw\\Brush\\Gradient
title: 'UI\\Draw\\Brush\\Gradient::setStop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Draw\\Brush\\Gradient::setStop

(UI 2.0.0)

UI\\Draw\\Brush\\Gradient::SetStop - Встановлює вузол градієнта

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

Колір для нового вузла, можливо UI\\Draw\\Color або RRGGBBAA.

### Значення, що повертаються

Індикація успіху.
