Елемент управління "Форма" (розташування)

-   [« UIControlsPicker::construct](ui-controls-picker.construct.html)
    
-   [ОЙControlsForm::append »](ui-controls-form.append.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Елемент управління "Форма" (розташування)
    

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

-   [ОЙControlsForm::append](ui-controls-form.append.html) — Додати елемент керування
-   [ОЙControlsForm::delete](ui-controls-form.delete.html) — Видалити елемент керування
-   [ОЙControlsForm::isPadded](ui-controls-form.ispadded.html) - Визначення заповнення
-   [ОЙControlsForm::setPadded](ui-controls-form.setpadded.html) - Встановити заповнення