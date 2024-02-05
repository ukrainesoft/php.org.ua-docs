---
navigation:
  - ui-controls-tab.setmargin.md: '« UI\\Controls\\Tab::setMargin'
  - ui-controls-check.construct.md: 'UI\\Controls\\Check::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Чекбокс"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Controls\\Check::\_\_construct](ui-controls-check.construct.md) \- Створити новий об'єкт Check
-   [UI\\Controls\\Check::getText](ui-controls-check.gettext.md)— Отримати текст
-   [UI\\Controls\\Check::isChecked](ui-controls-check.ischecked.md)— Визначення позначки
-   [UI\\Controls\\Check::onToggle](ui-controls-check.ontoggle.md)— Функція зворотного дзвінка перемикання
-   [UI\\Controls\\Check::setChecked](ui-controls-check.setchecked.md)— Встановити статус обраності
-   [UI\\Controls\\Check::setText](ui-controls-check.settext.md)— Встановити текст
