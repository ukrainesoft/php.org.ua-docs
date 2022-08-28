Елемент управління "Кнопка"

-   [« UI\\Controls\\Check::setText](ui-controls-check.settext.html)
    
-   [UI\\Controls\\Button::\_\_construct »](ui-controls-button.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Кнопка"
    

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

-   [UI\\Controls\\Button::\_\_construct](ui-controls-button.construct.html) — Створити новий об'єкт Button
-   [UI\\Controls\\Button::getText](ui-controls-button.gettext.html) — Отримати текст
-   [UI\\Controls\\Button::onClick](ui-controls-button.onclick.html) - Обробник кліку
-   [UI\\Controls\\Button::setText](ui-controls-button.settext.html) — Встановити текст