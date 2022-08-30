Елемент управління "Група" (розміщення)

-   [« UIControlsGrid::setPadded](ui-controls-grid.setpadded.html)
    
-   [ОЙControlsGroup::append »](ui-controls-group.append.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙ](book.ui.md)
    
-   Елемент управління "Група" (розміщення)
    

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

-   [ОЙControlsGroup::append](ui-controls-group.append.html) — Додати елемент керування
-   [ОЙControlsGroup::construct](ui-controls-group.construct.html) — Створити новий об'єкт Group
-   [ОЙControlsGroup::getTitle](ui-controls-group.gettitle.html) - Отримати заголовок
-   [ОЙControlsGroup::hasMargin](ui-controls-group.hasmargin.html) - Визначення поля
-   [ОЙControlsGroup::setMargin](ui-controls-group.setmargin.html) - Встановити поле
-   [ОЙControlsGroup::setTitle](ui-controls-group.settitle.html) - Встановити заголовок