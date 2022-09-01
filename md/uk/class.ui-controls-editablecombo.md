---
navigation:
  - ui-controls-combo.setselected.html: '« UIControlsCombo::setSelected'
  - ui-controls-editablecombo.append.html: 'ОЙControlsEditableCombo::append »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Редагований елемент управління "Комбо"
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

-   [ОЙControlsEditableCombo::append](ui-controls-editablecombo.append.html) - Додати опцію
-   [ОЙControlsEditableCombo::getText](ui-controls-editablecombo.gettext.html) — Отримати текст
-   [ОЙControlsEditableCombo::onChange](ui-controls-editablecombo.onchange.html) - Обробник зміни
-   [ОЙControlsEditableCombo::setText](ui-controls-editablecombo.settext.html) — Встановити текст
