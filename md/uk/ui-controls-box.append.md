---
navigation:
  - class.ui-controls-box.html: « UIControlsBox
  - ui-controls-box.construct.html: 'ОЙControlsBox::construct »'
  - index.md: PHP Manual
  - class.ui-controls-box.html: ОЙControlsBox
title: 'ОЙControlsBox::append'
---
# ОЙControlsBox::append

(UI 0.9.9)

ОЙControlsBox::append — Додати елемент керування

### Опис

```methodsynopsis
public UI\Controls\Box::append(Control $control, bool $stretchy = false): int
```

Додасть заданий керуючий елемент до цього блоку

### Список параметрів

`control`

Доданий елемент керування

`stretchy`

Встановити значення true, щоб розтягнути елемент керування

### Значення, що повертаються

Поверне індекс елемента управління, що додається, може бути значенням 0
