Елемент управління "Чекбокс"

-   [« UI\\Controls\\Tab::setMargin](ui-controls-tab.setmargin.html)
    
-   [UI\\Controls\\Check::\_\_construct »](ui-controls-check.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Чекбокс"
    

# Елемент управління "Чекбокс"

(UI 0.9.9)

## Вступ

Чекбокс (Check) є поміченим клікабельним блоком

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Check
     

     
      extends
       UI\Control
     
     {


    /* Конструктор */
    
   public __construct(string $text)


    /* Методы */
    public getText(): string
public isChecked(): bool
protected onToggle()
public setChecked(bool $checked)
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

-   [UI\\Controls\\Check::\_\_construct](ui-controls-check.construct.html) - Створити новий об'єкт Check
-   [UI\\Controls\\Check::getText](ui-controls-check.gettext.html) — Отримати текст
-   [UI\\Controls\\Check::isChecked](ui-controls-check.ischecked.html) — Визначення позначки
-   [UI\\Controls\\Check::onToggle](ui-controls-check.ontoggle.html) — Функція зворотного дзвінка перемикання
-   [UI\\Controls\\Check::setChecked](ui-controls-check.setchecked.html) — Встановити статус обраності
-   [UI\\Controls\\Check::setText](ui-controls-check.settext.html) — Встановити текст