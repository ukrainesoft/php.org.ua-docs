---
navigation:
  - ui-controls-editablecombo.settext.md: '« UI\\Controls\\EditableCombo::setText'
  - ui-controls-radio.append.md: 'UI\\Controls\\Radio::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Радіо"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Controls\\Radio::append](ui-controls-radio.append.md) \- Додає варіант
-   [UI\\Controls\\Radio::getSelected](ui-controls-radio.getselected.md)— Отримати вибраний варіант
-   [UI\\Controls\\Radio::onSelected](ui-controls-radio.onselected.md) \- Обробник вибору
-   [UI\\Controls\\Radio::setSelected](ui-controls-radio.setselected.md)— Встановити вибраний варіант
