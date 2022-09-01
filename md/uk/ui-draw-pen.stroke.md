---
navigation:
  - ui-draw-pen.save.html: '« UIDrawPen::save'
  - ui-draw-pen.transform.html: 'ОЙDrawPen::transform »'
  - index.md: PHP Manual
  - class.ui-draw-pen.html: ОЙDrawPen
title: 'ОЙDrawPen::stroke'
---
# ОЙDrawPen::stroke

(UI 0.9.9)

ОЙDrawPen::stroke — Обвести шлях

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
