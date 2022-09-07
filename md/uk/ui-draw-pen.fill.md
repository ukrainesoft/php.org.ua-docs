---
navigation:
  - ui-draw-pen.clip.md: '« UIDrawPen::clip'
  - ui-draw-pen.restore.md: 'ОЙDrawPen::restore »'
  - index.md: PHP Manual
  - class.ui-draw-pen.md: ОЙDrawPen
title: 'ОЙDrawPen::fill'
---
# ОЙDrawPen::fill

(UI 0.9.9)

ОЙDrawPen::fill - Залити шлях

### Опис

```methodsynopsis
public UI\Draw\Pen::fill(UI\Draw\Path $path, UI\Draw\Brush $with)
```

```methodsynopsis
public UI\Draw\Pen::fill(UI\Draw\Path $path, UI\Draw\Color $with)
```

```methodsynopsis
public UI\Draw\Pen::fill(UI\Draw\Path $path, int $with)
```

Заливає заданий шлях

### Список параметрів

`path`

Шлях для заливання

`with`

Колір або пензель для заливки
