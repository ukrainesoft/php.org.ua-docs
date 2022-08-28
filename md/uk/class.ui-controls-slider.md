Елемент управління "Слайдер"

-   [« UI\\Controls\\Spin::setValue](ui-controls-spin.setvalue.html)
    
-   [UI\\Controls\\Slider::\_\_construct »](ui-controls-slider.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Слайдер"
    

# Елемент управління "Слайдер"

(UI 0.9.9)

## Вступ

Слайдер - це елемент управління, що представляє діапазон та поточне значення у ньому. Ковзаючий елемент управління (іноді званий "великим пальцем") відображає значення і може бути відрегульований в межах діапазону.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Slider
     

     
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

-   [UI\\Controls\\Slider::\_\_construct](ui-controls-slider.construct.html) — Створює новий об'єкт Slider
-   [UI\\Controls\\Slider::getValue](ui-controls-slider.getvalue.html) — Отримати значення
-   [UI\\Controls\\Slider::onChange](ui-controls-slider.onchange.html) - Обробник зміни
-   [UI\\Controls\\Slider::setValue](ui-controls-slider.setvalue.html) — Встановити значення