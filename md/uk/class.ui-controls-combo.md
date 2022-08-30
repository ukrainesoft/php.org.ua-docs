Елемент управління "Комбо"

-   [« UIControlsSeparator::construct](ui-controls-separator.construct.html)
    
-   [ОЙControlsCombo::append »](ui-controls-combo.append.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
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

-   [ОЙControlsCombo::append](ui-controls-combo.append.html) - Додати опцію
-   [ОЙControlsCombo::getSelected](ui-controls-combo.getselected.html) — Отримати вибрану опцію
-   [ОЙControlsCombo::onSelected](ui-controls-combo.onselected.html) - Обробник обраної опції
-   [ОЙControlsCombo::setSelected](ui-controls-combo.setselected.html) — Встановлює вибрану опцію