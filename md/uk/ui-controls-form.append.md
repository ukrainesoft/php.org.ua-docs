---
navigation:
  - class.ui-controls-form.md: « UIControlsForm
  - ui-controls-form.delete.md: 'ОЙControlsForm::delete »'
  - index.md: PHP Manual
  - class.ui-controls-form.md: ОЙControlsForm
title: 'ОЙControlsForm::append'
---
# ОЙControlsForm::append

(UI 0.9.9)

ОЙControlsForm::append — Додати елемент керування

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
