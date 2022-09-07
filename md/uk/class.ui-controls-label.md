---
navigation:
  - ui-controls-colorbutton.setcolor.md: '« UIControlsColorButton::setColor'
  - ui-controls-label.construct.md: 'ОЙControlsLabel::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Мітка"
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

-   [ОЙControlsLabel::construct](ui-controls-label.construct.md) - Створити новий об'єкт Label
-   [ОЙControlsLabel::getText](ui-controls-label.gettext.md) — Отримати текст
-   [ОЙControlsLabel::setText](ui-controls-label.settext.md) — Встановити текст
