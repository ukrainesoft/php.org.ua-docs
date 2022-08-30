Додати керуючий елемент

-   [« UIControlsForm](class.ui-controls-form.html)
    
-   [ОЙControlsForm::delete »](ui-controls-form.delete.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙControlsForm](class.ui-controls-form.html)
    
-   Додати керуючий елемент
    

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