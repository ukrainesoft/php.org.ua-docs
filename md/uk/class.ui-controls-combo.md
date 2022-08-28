Елемент управління "Комбо"

-   [« UI\\Controls\\Separator::\_\_construct](ui-controls-separator.construct.html)
    
-   [UI\\Controls\\Combo::append »](ui-controls-combo.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Комбо"
    

# Елемент управління "Комбо"

(UI 0.9.9)

## Вступ

Елемент управління "Комбо" представляє список опцій, наприклад схожий на HTML-елемент.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Combo
     

     
      extends
       UI\Control
     
     {


    /* Методы */
    
   public append(string $text)
public getSelected(): int
protected onSelected()
public setSelected(int $index)


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

-   [UI\\Controls\\Combo::append](ui-controls-combo.append.html) - Додати опцію
-   [UI\\Controls\\Combo::getSelected](ui-controls-combo.getselected.html) — Отримати вибрану опцію
-   [UI\\Controls\\Combo::onSelected](ui-controls-combo.onselected.html) - Обробник обраної опції
-   [UI\\Controls\\Combo::setSelected](ui-controls-combo.setselected.html) — Встановлює вибрану опцію