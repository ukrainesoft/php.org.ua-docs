Елемент управління "Спін"

-   [« UIControlsMultilineEntry::setText](ui-controls-multilineentry.settext.html)
    
-   [ОЙControlsSpin::construct »](ui-controls-spin.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Елемент управління "Спін"
    

# Елемент управління "Спін"

(UI 0.9.9)

## Вступ

Блок "Спин" представляє текстове поле з елементом управління "вгору", який змінює ціле значення в полі, в межах заданого діапазону

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Spin
     

     
      extends
       UI\Control
     
     {


    /* Конструктор */
    
   public __construct(int $min, int $max)


    /* Методы */
    public getValue(): int
protected onChange()
public setValue(int $value)


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

## Зміст

-   [ОЙControlsSpin::construct](ui-controls-spin.construct.html) - Створює новий об'єкт Spin
-   [ОЙControlsSpin::getValue](ui-controls-spin.getvalue.html) — Отримати значення
-   [ОЙControlsSpin::onChange](ui-controls-spin.onchange.html) - Обробник зміни
-   [ОЙControlsSpin::setValue](ui-controls-spin.setvalue.html) — Встановити значення