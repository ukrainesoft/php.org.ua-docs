---
navigation:
  - ui-controls-colorbutton.setcolor.md: '« UI\\Controls\\ColorButton::setColor'
  - ui-controls-label.construct.md: 'UI\\Controls\\Label::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Мітка"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління "Мітка"

(UI 0.9.9)

## Вступ

Мітка представляє один рядок тексту, призначений для ідентифікації користувача певного елемента інтерфейсу.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Label
     

     
      extends
       UI\Control
     
     {


    /* Конструктор */
    
   public __construct(string $text)


    /* Методы */
    public getText(): string
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

-   [UI\\Controls\\Label::\_\_construct](ui-controls-label.construct.md) \- Створити новий об'єкт Label
-   [UI\\Controls\\Label::getText](ui-controls-label.gettext.md)— Отримати текст
-   [UI\\Controls\\Label::setText](ui-controls-label.settext.md)— Встановити текст
