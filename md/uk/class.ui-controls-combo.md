---
navigation:
  - ui-controls-separator.construct.md: '« UI\\Controls\\Separator::\_\_construct'
  - ui-controls-combo.append.md: 'UI\\Controls\\Combo::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Комбо"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Controls\\Combo::append](ui-controls-combo.append.md) \- Додати опцію
-   [UI\\Controls\\Combo::getSelected](ui-controls-combo.getselected.md)— Отримати вибрану опцію
-   [UI\\Controls\\Combo::onSelected](ui-controls-combo.onselected.md) \- Обробник обраної опції
-   [UI\\Controls\\Combo::setSelected](ui-controls-combo.setselected.md)— Встановлює вибрану опцію
