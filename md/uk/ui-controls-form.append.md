---
navigation:
  - class.ui-controls-form.md: « UI\\Controls\\Form
  - ui-controls-form.delete.md: 'UI\\Controls\\Form::delete »'
  - index.md: PHP Manual
  - class.ui-controls-form.md: UI\\Controls\\Form
title: 'UI\\Controls\\Form::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Controls\\Form::append

(UI 0.9.9)

UI\\Controls\\Form::append — Додати елемент керування

### Опис

```methodsynopsis
public UI\Controls\Form::append(string $label, UI\Control $control, bool $stretchy = false): int
```

Додає елемент управління до форми та встановлює мітку

### Список параметрів

`label`

Текст для мітки

`control`

Керуючий елемент

`stretchy`

Має значення true, щоб розтягнути елемент управління

### Значення, що повертаються

Повертає індекс доданого елемента управління, можливо значення 0
