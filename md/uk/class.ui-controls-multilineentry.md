---
navigation:
  - ui-controls-entry.settext.html: '« UIControlsEntry::setText'
  - ui-controls-multilineentry.append.html: 'ОЙControlsMultilineEntry::append »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Елемент управління "Многорядкове введення"
---
# Елемент управління "Многорядкове введення"

(UI 0.9.9)

## Вступ

Багаторядкове введення - це елемент керування текстового запису, здатний зберігати кілька рядків тексту, з перенесенням рядків або без нього.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\MultilineEntry
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Wrap;

    const
     int
      NoWrap;


    /* Конструктор */
    
   public __construct(int $type = ?)


    /* Методы */
    public append(string $text)
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

**`UI\Controls\MultilineEntry::Wrap`**

Дозволити перенесення рядків

**`UI\Controls\MultilineEntry::NoWrap`**

Не дозволяти перенесення рядків

## Зміст

-   [ОЙControlsMultilineEntry::append](ui-controls-multilineentry.append.html) — Додати текст
-   [ОЙControlsMultilineEntry::construct](ui-controls-multilineentry.construct.html) - Створити новий об'єкт "Многорядкове введення"
-   [ОЙControlsMultilineEntry::getText](ui-controls-multilineentry.gettext.html) — Отримати текст
-   [ОЙControlsMultilineEntry::isReadOnly](ui-controls-multilineentry.isreadonly.html) - Визначення "тільки для читання"
-   [ОЙControlsMultilineEntry::onChange](ui-controls-multilineentry.onchange.html) - Обробник зміни
-   [ОЙControlsMultilineEntry::setReadOnly](ui-controls-multilineentry.setreadonly.html) - Встановити "тільки для читання"
-   [ОЙControlsMultilineEntry::setText](ui-controls-multilineentry.settext.html) — Встановити текст
