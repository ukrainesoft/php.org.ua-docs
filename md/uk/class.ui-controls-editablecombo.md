---
navigation:
  - ui-controls-combo.setselected.md: '« UI\\Controls\\Combo::setSelected'
  - ui-controls-editablecombo.append.md: 'UI\\Controls\\EditableCombo::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Редагований елемент управління "Комбо"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Редагований елемент управління "Комбо"

(UI 0.9.9)

## Вступ

Редагований елемент керування "Комбо" дозволяє користувачеві вводити довільні опції

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\EditableCombo
     

     
      extends
       UI\Control
     
     {


    /* Методы */
    
   public append(string $text)
public getText(): string
protected onChange()
public setText(string $text)


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

-   [UI\\Controls\\EditableCombo::append](ui-controls-editablecombo.append.md) \- Додати опцію
-   [UI\\Controls\\EditableCombo::getText](ui-controls-editablecombo.gettext.md)— Отримати текст
-   [UI\\Controls\\EditableCombo::onChange](ui-controls-editablecombo.onchange.md) \- Обробник зміни
-   [UI\\Controls\\EditableCombo::setText](ui-controls-editablecombo.settext.md)— Встановити текст
