Елемент управління "Радіо"

-   [« UI\\Controls\\EditableCombo::setText](ui-controls-editablecombo.settext.html)
    
-   [UI\\Controls\\Radio::append »](ui-controls-radio.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Елемент управління "Радіо"
    

# Елемент управління "Радіо"

(UI 0.9.9)

## Вступ

Радіо схожий на радіокнопку з HTML

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Radio
     

     
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

-   [UI\\Controls\\Radio::append](ui-controls-radio.append.html) - Додає варіант
-   [UI\\Controls\\Radio::getSelected](ui-controls-radio.getselected.html) — Отримати вибраний варіант
-   [UI\\Controls\\Radio::onSelected](ui-controls-radio.onselected.html) - Обробник вибору
-   [UI\\Controls\\Radio::setSelected](ui-controls-radio.setselected.html) — Встановити вибраний варіант