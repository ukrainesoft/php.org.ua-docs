Елемент управління "Радіо"

-   [« UIControlsEditableCombo::setText](ui-controls-editablecombo.settext.html)
    
-   [ОЙControlsRadio::append »](ui-controls-radio.append.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙ](book.ui.md)
    
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

-   [ОЙControlsRadio::append](ui-controls-radio.append.html) - Додає варіант
-   [ОЙControlsRadio::getSelected](ui-controls-radio.getselected.html) — Отримати вибраний варіант
-   [ОЙControlsRadio::onSelected](ui-controls-radio.onselected.html) - Обробник вибору
-   [ОЙControlsRadio::setSelected](ui-controls-radio.setselected.html) — Встановити вибраний варіант