---
navigation:
  - ui-executor.setinterval.md: '« UIExecutor::setInterval'
  - ui-controls-tab.append.md: 'ОЙControlsTab::append »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління "Таб"
---
# Елемент управління "Таб"

(UI 0.9.9)

## Вступ

Таб може містити багато вибраних користувачем сторінок елементів управління, кожна з якої має заголовок.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Tab
     

     
      extends
       UI\Control
     
     {


    /* Свойства */
    
     protected
      $controls;


    /* Методы */
    
   public append(string $name, UI\Control $control): int
public delete(int $index): bool
public hasMargin(int $page): bool
public insertAt(string $name, int $page, UI\Control $control)
public pages(): int
public setMargin(int $page, bool $margin)


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

## Властивості

controls

Містить елементи керування, не варто змінювати напряму

## Зміст

-   [ОЙControlsTab::append](ui-controls-tab.append.md) - Додати сторінку
-   [ОЙControlsTab::delete](ui-controls-tab.delete.md) — Видалити сторінку
-   [ОЙControlsTab::hasMargin](ui-controls-tab.hasmargin.md) - Визначення поля
-   [ОЙControlsTab::insertAt](ui-controls-tab.insertat.md) - Вставити сторінку
-   [ОЙControlsTab::pages](ui-controls-tab.pages.md) - Кількість сторінок
-   [ОЙControlsTab::setMargin](ui-controls-tab.setmargin.md) - Встановити поле
