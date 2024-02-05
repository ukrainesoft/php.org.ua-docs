---
navigation:
  - ui-controls-grid.setpadded.md: '« UI\\Controls\\Grid::setPadded'
  - ui-controls-group.append.md: 'UI\\Controls\\Group::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління "Група" (розміщення)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління "Група" (розміщення)

(UI 0.9.9)

## Вступ

Група представляє контейнер для дочірніх елементів

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Group
     

     
      extends
       UI\Control
     
     {


    /* Свойства */
    
     protected
      $controls;


    /* Конструктор */
    
   public __construct(string $title)


    /* Методы */
    public append(UI\Control $control)
public getTitle(): string
public hasMargin(): bool
public setMargin(bool $margin)
public setTitle(string $title)


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

-   [UI\\Controls\\Group::append](ui-controls-group.append.md)— Додати елемент керування
-   [UI\\Controls\\Group::\_\_construct](ui-controls-group.construct.md)— Створити новий об'єкт Group
-   [UI\\Controls\\Group::getTitle](ui-controls-group.gettitle.md) \- Отримати заголовок
-   [UI\\Controls\\Group::hasMargin](ui-controls-group.hasmargin.md) \- Визначення поля
-   [UI\\Controls\\Group::setMargin](ui-controls-group.setmargin.md) \- Встановити поле
-   [UI\\Controls\\Group::setTitle](ui-controls-group.settitle.md) \- Встановити заголовок
