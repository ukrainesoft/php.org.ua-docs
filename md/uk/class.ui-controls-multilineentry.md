Елемент управління "Многорядкове введення"

-   [« UI\\Controls\\Entry::setText](ui-controls-entry.settext.html)
    
-   [UI\\Controls\\MultilineEntry::append »](ui-controls-multilineentry.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Многорядкове введення"
    

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

-   [UI\\Controls\\MultilineEntry::append](ui-controls-multilineentry.append.html) — Додати текст
-   [UI\\Controls\\MultilineEntry::\_\_construct](ui-controls-multilineentry.construct.html) - Створити новий об'єкт "Многорядкове введення"
-   [UI\\Controls\\MultilineEntry::getText](ui-controls-multilineentry.gettext.html) — Отримати текст
-   [UI\\Controls\\MultilineEntry::isReadOnly](ui-controls-multilineentry.isreadonly.html) - Визначення "тільки для читання"
-   [UI\\Controls\\MultilineEntry::onChange](ui-controls-multilineentry.onchange.html) - Обробник зміни
-   [UI\\Controls\\MultilineEntry::setReadOnly](ui-controls-multilineentry.setreadonly.html) - Встановити "тільки для читання"
-   [UI\\Controls\\MultilineEntry::setText](ui-controls-multilineentry.settext.html) — Встановити текст