---
navigation:
  - class.ui-area.md: « UI\\Area
  - ui-area.onkey.md: 'UI\\Area::onKey »'
  - index.md: PHP Manual
  - class.ui-area.md: UI\\Area
title: 'UI\\Area::onDraw'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Area::onDraw

(UI 0.9.9)

UI\\Area::onDraw - Функція зворотного виклику при малюванні

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
