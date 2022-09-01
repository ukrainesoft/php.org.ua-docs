---
navigation:
  - ui-controls-button.settext.html: '« UIControlsButton::setText'
  - ui-controls-colorbutton.getcolor.html: 'ОЙControlsColorButton::getColor »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Кнопка з палітрою кольорів"
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

-   [ОЙControlsColorButton::getColor](ui-controls-colorbutton.getcolor.html) — Отримати об'єкт Color
-   [ОЙControlsColorButton::onChange](ui-controls-colorbutton.onchange.html) - Обробник зміни
-   [ОЙControlsColorButton::setColor](ui-controls-colorbutton.setcolor.html) — Встановити об'єкт Color
