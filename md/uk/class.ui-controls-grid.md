---
navigation:
  - ui-controls-form.setpadded.md: '« UIControlsForm::setPadded'
  - ui-controls-grid.append.md: 'ОЙControlsGrid::append »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Сітка" (розміщення)
---
# Елемент управління "Сітка" (розміщення)

(UI 0.9.9)

## Вступ

Сітка - це елемент керування, що дозволяє розміщувати дочірні елементи у сітці

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Grid
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Fill;

    const
     int
      Start;

    const
     int
      Center;

    const
     int
      End;

    const
     int
      Leading;

    const
     int
      Top;

    const
     int
      Trailing;

    const
     int
      Bottom;


    /* Свойства */
    protected
      $controls;


    /* Методы */
    
   public append(    UI\Control $control,    int $left,    int $top,    int $xspan,    int $yspan,    bool $hexpand,    int $halign,    bool $vexpand,    int $valign)
public isPadded(): bool
public setPadded(bool $padding)


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

**`UI\Controls\Grid::Fill`**

**`UI\Controls\Grid::Start`**

**`UI\Controls\Grid::Center`**

**`UI\Controls\Grid::End`**

**`UI\Controls\Grid::Leading`**

**`UI\Controls\Grid::Top`**

**`UI\Controls\Grid::Trailing`**

**`UI\Controls\Grid::Bottom`**

## Властивості

controls

Містить елементи керування, не варто змінювати напряму

## Зміст

-   [ОЙControlsGrid::append](ui-controls-grid.append.md) — Додати елемент керування
-   [ОЙControlsGrid::isPadded](ui-controls-grid.ispadded.md) - Визначення заповнення
-   [ОЙControlsGrid::setPadded](ui-controls-grid.setpadded.md) - Встановити заповнення
