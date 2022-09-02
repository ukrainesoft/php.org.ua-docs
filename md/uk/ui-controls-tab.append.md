---
navigation:
  - class.ui-controls-tab.md: « UIControlsTab
  - ui-controls-tab.delete.md: 'ОЙControlsTab::delete »'
  - index.md: PHP Manual
  - class.ui-controls-tab.md: ОЙControlsTab
title: 'ОЙControlsTab::append'
---
# ОЙControlsTab::append

(UI 0.9.9)

ОЙControlsTab::append — Додати сторінку

### Опис

```methodsynopsis
public UI\Controls\Tab::append(string $name, UI\Control $control): int
```

Додати нову сторінку до цього керуючого елементу "Таб"

### Список параметрів

`name`

Назва нової сторінки

`control`

Керуючий елемент для нової сторінки

### Значення, що повертаються

Повертає індекс доданого елемента управління, можливо значення 0
