---
navigation:
  - ui-controls-label.settext.md: '« UI\\Controls\\Label::setText'
  - ui-controls-entry.construct.md: 'UI\\Controls\\Entry::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Введення"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління "Введення"

(UI 0.9.9)

## Вступ

Введення (Entry) - елемент керування текстовим записом, який підходить для введення простого тексту, паролів або пошукових запитів.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Entry
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Normal;

    const
     int
      Password;

    const
     int
      Search;


    /* Конструктор */
    
   public __construct(int $type = UI\Controls\Entry::Normal)


    /* Методы */
    public getText(): string
public isReadOnly(): bool
protected onChange()
public setReadOnly(bool $readOnly)
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

## Обумовлені константи

**`UI\Controls\Entry::Normal`**

Звичайне однорядкове введення

**`UI\Controls\Entry::Password`**

Введення пароля

**`UI\Controls\Entry::Search`**

Введення пошуку

## Зміст

-   [UI\\Controls\\Entry::\_\_construct](ui-controls-entry.construct.md)— Створити новий об'єкт Entry
-   [UI\\Controls\\Entry::getText](ui-controls-entry.gettext.md)— Отримати текст
-   [UI\\Controls\\Entry::isReadOnly](ui-controls-entry.isreadonly.md)— Визначити, чи є елемент лише для читання
-   [UI\\Controls\\Entry::onChange](ui-controls-entry.onchange.md) \- Обробник зміни
-   [UI\\Controls\\Entry::setReadOnly](ui-controls-entry.setreadonly.md) - Встановити "тільки для читання"
-   [UI\\Controls\\Entry::setText](ui-controls-entry.settext.md)— Встановити текст
