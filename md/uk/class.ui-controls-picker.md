---
navigation:
  - ui-controls-radio.setselected.md: '« UI\\Controls\\Radio::setSelected'
  - ui-controls-picker.construct.md: 'UI\\Controls\\Picker::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент керування "Селектор"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент керування "Селектор"

(UI 0.9.9)

## Вступ

Селектор представляє кнопку, яка при натисканні відкриває нативний інтерфейс селектора дати/часу/дати та часу.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Picker
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Date;

    const
     int
      Time;

    const
     int
      DateTime;


    /* Конструктор */
    
   public __construct(int $type = UI\Controls\Picker::Date)


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

## Обумовлені константи

**`UI\Controls\Picker::Date`**

Селектор дати

**`UI\Controls\Picker::Time`**

Селектор часу

**`UI\Controls\Picker::DateTime`**

Селектор дати та часу

## Зміст

-   [UI\\Controls\\Picker::\_\_construct](ui-controls-picker.construct.md) \- Створює новий об'єкт Picker
