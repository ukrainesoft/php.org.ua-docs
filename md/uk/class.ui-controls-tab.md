---
navigation:
  - ui-executor.setinterval.md: '« UI\\Executor::setInterval'
  - ui-controls-tab.append.md: 'UI\\Controls\\Tab::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Таб"
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Controls\\Tab::append](ui-controls-tab.append.md) \- Додати сторінку
-   [UI\\Controls\\Tab::delete](ui-controls-tab.delete.md)— Видалити сторінку
-   [UI\\Controls\\Tab::hasMargin](ui-controls-tab.hasmargin.md) \- Визначення поля
-   [UI\\Controls\\Tab::insertAt](ui-controls-tab.insertat.md) \- Вставити сторінку
-   [UI\\Controls\\Tab::pages](ui-controls-tab.pages.md) \- Кількість сторінок
-   [UI\\Controls\\Tab::setMargin](ui-controls-tab.setmargin.md) \- Встановити поле
