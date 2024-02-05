---
navigation:
  - ui-controls-check.settext.md: '« UI\\Controls\\Check::setText'
  - ui-controls-button.construct.md: 'UI\\Controls\\Button::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Кнопка"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Controls\\Button::\_\_construct](ui-controls-button.construct.md)— Створити новий об'єкт Button
-   [UI\\Controls\\Button::getText](ui-controls-button.gettext.md)— Отримати текст
-   [UI\\Controls\\Button::onClick](ui-controls-button.onclick.md) \- Обробник кліку
-   [UI\\Controls\\Button::setText](ui-controls-button.settext.md)— Встановити текст
