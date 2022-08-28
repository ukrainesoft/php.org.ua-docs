Елемент управління "Група" (розміщення)

-   [« UI\\Controls\\Grid::setPadded](ui-controls-grid.setpadded.html)
    
-   [UI\\Controls\\Group::append »](ui-controls-group.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
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

-   [UI\\Controls\\Group::append](ui-controls-group.append.html) — Додати елемент керування
-   [UI\\Controls\\Group::\_\_construct](ui-controls-group.construct.html) — Створити новий об'єкт Group
-   [UI\\Controls\\Group::getTitle](ui-controls-group.gettitle.html) - Отримати заголовок
-   [UI\\Controls\\Group::hasMargin](ui-controls-group.hasmargin.html) - Визначення поля
-   [UI\\Controls\\Group::setMargin](ui-controls-group.setmargin.html) - Встановити поле
-   [UI\\Controls\\Group::setTitle](ui-controls-group.settitle.html) - Встановити заголовок