---
navigation:
  - ui-controls-button.settext.md: '« UI\\Controls\\Button::setText'
  - ui-controls-colorbutton.getcolor.md: 'UI\\Controls\\ColorButton::getColor »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Кнопка з палітрою кольорів"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Controls\\ColorButton::getColor](ui-controls-colorbutton.getcolor.md)— Отримати об'єкт Color
-   [UI\\Controls\\ColorButton::onChange](ui-controls-colorbutton.onchange.md) \- Обробник зміни
-   [UI\\Controls\\ColorButton::setColor](ui-controls-colorbutton.setcolor.md)— Встановити об'єкт Color
