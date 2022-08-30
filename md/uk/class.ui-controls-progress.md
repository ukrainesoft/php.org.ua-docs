Елемент управління "Хід виконання"

-   [« UIControlsSlider::setValue](ui-controls-slider.setvalue.html)
    
-   [ОЙControlsProgress::getValue »](ui-controls-progress.getvalue.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Елемент управління "Хід виконання"
    

# Елемент управління "Хід виконання"

(UI 0.9.9)

## Вступ

Елемент управління "Хід виконання" схожий на знайомий індикатор виконання: Він є індикатором виконання у відсотках з допустимим діапазоном від 0 до 100 (включно).

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Progress
     

     
      extends
       UI\Control
     
     {


    /* Методы */
    
   public getValue(): int
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

-   [ОЙControlsProgress::getValue](ui-controls-progress.getvalue.html) — Отримати значення
-   [ОЙControlsProgress::setValue](ui-controls-progress.setvalue.html) — Встановити значення