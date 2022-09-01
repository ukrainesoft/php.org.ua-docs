---
navigation:
  - ui-controls-editablecombo.settext.html: '« UIControlsEditableCombo::setText'
  - ui-controls-radio.append.html: 'ОЙControlsRadio::append »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Радіо"
---
# Елемент управління "Радіо"

(UI 0.9.9)

## Вступ

Радіо схожий на радіокнопку з HTML

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Radio
     

     
      extends
       UI\Control
     
     {


    /* Методы */
    
   public append(string $text)
public getSelected(): int
protected onSelected()
public setSelected(int $index)


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

-   [ОЙControlsRadio::append](ui-controls-radio.append.md) - Додає варіант
-   [ОЙControlsRadio::getSelected](ui-controls-radio.getselected.md) — Отримати вибраний варіант
-   [ОЙControlsRadio::onSelected](ui-controls-radio.onselected.md) - Обробник вибору
-   [ОЙControlsRadio::setSelected](ui-controls-radio.setselected.md) — Встановити вибраний варіант
