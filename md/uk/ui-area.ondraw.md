---
navigation:
  - class.ui-area.html: « UIArea
  - ui-area.onkey.html: 'ОЙArea::onKey »'
  - index.html: PHP Manual
  - class.ui-area.html: ОЙArea
title: 'ОЙArea::onDraw'
---
# ОЙArea::onDraw

(UI 0.9.9)

ОЙArea::onDraw - Функція зворотного виклику при малюванні

### Опис

```methodsynopsis
protected UI\Area::onDraw(    UI\Draw\Pen $pen,    UI\Size $areaSize,    UI\Point $clipPoint,    UI\Size $clipSize)
```

Викликається, коли ця область вимагає перемальовки

### Список параметрів

`pen`

Ручка (Pen), що підходить для малювання у цьому районі

`areaSize`

Розмір області

`clipPoint`

Точка обрізки (clip point) області

`clipSize`

Розмір обрізки (clip size) області
