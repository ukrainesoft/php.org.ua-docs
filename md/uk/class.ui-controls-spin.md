---
navigation:
  - ui-controls-multilineentry.settext.md: '« UI\\Controls\\MultilineEntry::setText'
  - ui-controls-spin.construct.md: 'UI\\Controls\\Spin::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Спін"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Controls\\Spin::\_\_construct](ui-controls-spin.construct.md) \- Створює новий об'єкт Spin
-   [UI\\Controls\\Spin::getValue](ui-controls-spin.getvalue.md)— Отримати значення
-   [UI\\Controls\\Spin::onChange](ui-controls-spin.onchange.md) \- Обробник зміни
-   [UI\\Controls\\Spin::setValue](ui-controls-spin.setvalue.md)— Встановити значення
