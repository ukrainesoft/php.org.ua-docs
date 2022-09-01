---
navigation:
  - ui-controls-check.settext.html: '« UIControlsCheck::setText'
  - ui-controls-button.construct.html: 'ОЙControlsButton::construct »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Елемент управління "Кнопка"
---
# Елемент управління "Кнопка"

(UI 0.9.9)

## Вступ

Являє собою позначену клікабельну кнопку

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Button
     

     
      extends
       UI\Control
     
     {


    /* Конструктор */
    
   public __construct(string $text)


    /* Методы */
    public getText(): string
protected onClick()
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

-   [ОЙControlsButton::construct](ui-controls-button.construct.html) — Створити новий об'єкт Button
-   [ОЙControlsButton::getText](ui-controls-button.gettext.html) — Отримати текст
-   [ОЙControlsButton::onClick](ui-controls-button.onclick.html) - Обробник кліку
-   [ОЙControlsButton::setText](ui-controls-button.settext.html) — Встановити текст
