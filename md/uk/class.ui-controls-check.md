---
navigation:
  - ui-controls-tab.setmargin.md: '« UIControlsTab::setMargin'
  - ui-controls-check.construct.md: 'ОЙControlsCheck::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
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

-   [ОЙControlsCheck::construct](ui-controls-check.construct.md) - Створити новий об'єкт Check
-   [ОЙControlsCheck::getText](ui-controls-check.gettext.md) — Отримати текст
-   [ОЙControlsCheck::isChecked](ui-controls-check.ischecked.md) — Визначення позначки
-   [ОЙControlsCheck::onToggle](ui-controls-check.ontoggle.md) — Функція зворотного дзвінка перемикання
-   [ОЙControlsCheck::setChecked](ui-controls-check.setchecked.md) — Встановити статус обраності
-   [ОЙControlsCheck::setText](ui-controls-check.settext.md) — Встановити текст
