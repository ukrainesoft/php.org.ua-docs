Елемент управління "Мітка"

-   [« UI\\Controls\\ColorButton::setColor](ui-controls-colorbutton.setcolor.html)
    
-   [UI\\Controls\\Label::\_\_construct »](ui-controls-label.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Мітка"
    

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

-   [UI\\Controls\\Label::\_\_construct](ui-controls-label.construct.html) - Створити новий об'єкт Label
-   [UI\\Controls\\Label::getText](ui-controls-label.gettext.html) — Отримати текст
-   [UI\\Controls\\Label::setText](ui-controls-label.settext.html) — Встановити текст