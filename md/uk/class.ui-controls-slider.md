---
navigation:
  - ui-controls-spin.setvalue.md: '« UIControlsSpin::setValue'
  - ui-controls-slider.construct.md: 'ОЙControlsSlider::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Слайдер"
---
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

-   [ОЙControlsSlider::construct](ui-controls-slider.construct.md) — Створює новий об'єкт Slider
-   [ОЙControlsSlider::getValue](ui-controls-slider.getvalue.md) — Отримати значення
-   [ОЙControlsSlider::onChange](ui-controls-slider.onchange.md) - Обробник зміни
-   [ОЙControlsSlider::setValue](ui-controls-slider.setvalue.md) — Встановити значення
