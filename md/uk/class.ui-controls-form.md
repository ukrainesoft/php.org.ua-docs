---
navigation:
  - ui-controls-picker.construct.md: '« UI\\Controls\\Picker::\_\_construct'
  - ui-controls-form.append.md: 'UI\\Controls\\Form::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Форма" (розташування)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління "Форма" (розташування)

(UI 0.9.9)

## Вступ

Форма - це елемент управління, що дозволяє розміщувати інші елементи управління у макеті (формі).

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Form
     

     
      extends
       UI\Control
     
     {


    /* Свойства */
    
     protected
      $controls;


    /* Методы */
    
   public append(string $label, UI\Control $control, bool $stretchy = false): int
public delete(int $index): bool
public isPadded(): bool
public setPadded(bool $padded)


    /* Наследуемые методы */
    public UI\Control::destroy()
public UI\Control::disable()
public UI\Control::enable()
public UI\Control::getParent(): UI\Control
public UI\Control::getTopLevel(): int
public UI\Control::hide()
public UI\Control::isEnabled(): bool
public UI\Control::isVisible(): bool
public UI\Control::setParent(UI\Control $parent)
public UI\Control::show()


   }
```

## Властивості

controls

Містить елементи керування, не варто змінювати напряму

## Зміст

-   [UI\\Controls\\Form::append](ui-controls-form.append.md)— Додати елемент керування
-   [UI\\Controls\\Form::delete](ui-controls-form.delete.md)— Видалити елемент керування
-   [UI\\Controls\\Form::isPadded](ui-controls-form.ispadded.md) \- Визначення заповнення
-   [UI\\Controls\\Form::setPadded](ui-controls-form.setpadded.md) \- Встановити заповнення
