---
navigation:
  - ui-draw-pen.save.md: '« UI\\Draw\\Pen::save'
  - ui-draw-pen.transform.md: 'UI\\Draw\\Pen::transform »'
  - index.md: PHP Manual
  - class.ui-draw-pen.md: UI\\Draw\\Pen
title: 'UI\\Draw\\Pen::stroke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Draw\\Pen::stroke

(UI 0.9.9)

UI\\Draw\\Pen::stroke — Обвести шлях

### Опис

```methodsynopsis
public UI\Draw\Pen::stroke(UI\Draw\Path $path, UI\Draw\Brush $with, UI\Draw\Stroke $stroke)
```

```methodsynopsis
public UI\Draw\Pen::stroke(UI\Draw\Path $path, UI\Draw\Color $with, UI\Draw\Stroke $stroke)
```

```methodsynopsis
public UI\Draw\Pen::stroke(UI\Draw\Path $path, int $with, UI\Draw\Stroke $stroke)
```

Обведе шлях

### Список параметрів

`path`

Шлях для обведення

`with`

Колір або пензель, щоб обвести

`stroke`

Конфігурація обведення
