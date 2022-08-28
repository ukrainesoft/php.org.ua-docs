Елемент управління "Кнопка з палітрою кольорів"

-   [« UI\\Controls\\Button::setText](ui-controls-button.settext.html)
    
-   [UI\\Controls\\ColorButton::getColor »](ui-controls-colorbutton.getcolor.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Кнопка з палітрою кольорів"
    

# Елемент управління "Кнопка з палітрою кольорів"

(UI 0.9.9)

## Вступ

Кнопка з палітрою кольорів – це кнопка, яка відображає селектор кольору при натисканні

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\ColorButton
     

     
      extends
       UI\Control
     
     {


    /* Методы */
    
   public getColor(): UI\Color
protected onChange()
public setColor(UI\Draw\Color $color)
public setColor(int $color)


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

-   [UI\\Controls\\ColorButton::getColor](ui-controls-colorbutton.getcolor.html) — Отримати об'єкт Color
-   [UI\\Controls\\ColorButton::onChange](ui-controls-colorbutton.onchange.html) - Обробник зміни
-   [UI\\Controls\\ColorButton::setColor](ui-controls-colorbutton.setcolor.html) — Встановити об'єкт Color