---
navigation:
  - ui-controls-progress.setvalue.md: '« UI\\Controls\\Progress::setValue'
  - ui-controls-separator.construct.md: 'UI\\Controls\\Separator::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Розділювач"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління "Розділювач"

(UI 0.9.9)

## Вступ

Розділювач представляє елемент керування роздільника без будь-яких функцій.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Separator
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Horizontal;

    const
     int
      Vertical;


    /* Конструктор */
    
   public __construct(int $type = UI\Controls\Separator::Horizontal)


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

**`UI\Controls\Separator::Horizontal`**

Горизонтальний роздільник

**`UI\Controls\Separator::Vertical`**

Вертикальний роздільник

## Зміст

-   [UI\\Controls\\Separator::\_\_construct](ui-controls-separator.construct.md)— Створити новий об'єкт Separator
