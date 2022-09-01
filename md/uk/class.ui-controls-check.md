---
navigation:
  - ui-controls-tab.setmargin.html: '« UIControlsTab::setMargin'
  - ui-controls-check.construct.html: 'ОЙControlsCheck::construct »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Елемент управління "Чекбокс"
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

-   [ОЙControlsCheck::construct](ui-controls-check.construct.html) - Створити новий об'єкт Check
-   [ОЙControlsCheck::getText](ui-controls-check.gettext.html) — Отримати текст
-   [ОЙControlsCheck::isChecked](ui-controls-check.ischecked.html) — Визначення позначки
-   [ОЙControlsCheck::onToggle](ui-controls-check.ontoggle.html) — Функція зворотного дзвінка перемикання
-   [ОЙControlsCheck::setChecked](ui-controls-check.setchecked.html) — Встановити статус обраності
-   [ОЙControlsCheck::setText](ui-controls-check.settext.html) — Встановити текст
