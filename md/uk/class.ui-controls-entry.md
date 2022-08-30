Елемент управління "Введення"

-   [« UIControlsLabel::setText](ui-controls-label.settext.html)
    
-   [ОЙControlsEntry::construct »](ui-controls-entry.construct.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙ](book.ui.md)
    
-   Елемент управління "Введення"
    

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

-   [ОЙControlsEntry::construct](ui-controls-entry.construct.html) — Створити новий об'єкт Entry
-   [ОЙControlsEntry::getText](ui-controls-entry.gettext.html) — Отримати текст
-   [ОЙControlsEntry::isReadOnly](ui-controls-entry.isreadonly.html) — Визначити, чи є елемент лише для читання
-   [ОЙControlsEntry::onChange](ui-controls-entry.onchange.html) - Обробник зміни
-   [ОЙControlsEntry::setReadOnly](ui-controls-entry.setreadonly.html) - Встановити "тільки для читання"
-   [ОЙControlsEntry::setText](ui-controls-entry.settext.html) — Встановити текст