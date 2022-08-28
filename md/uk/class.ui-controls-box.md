Блок керування (розміщення)

-   [« UI\\Controls\\Group::setTitle](ui-controls-group.settitle.html)
    
-   [UI\\Controls\\Box::append »](ui-controls-box.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Блок керування (розміщення)
    

# Блок керування (розміщення)

(UI 0.9.9)

## Вступ

Блок (Box) дозволяє розташувати інші елементи керування

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Box
     

     
      extends
       UI\Control
     
     {


    /* Константы */
    
     const
     int
      Vertical;

    const
     int
      Horizontal;


    /* Свойства */
    protected
      $controls;


    /* Конструктор */
    
   public __construct(int $orientation = UI\Controls\Box::Horizontal)


    /* Методы */
    public append(Control $control, bool $stretchy = false): int
public delete(int $index): bool
public getOrientation(): int
public isPadded(): bool
public setPadded(bool $padded)


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

Містить елементи керування, не слід використовувати безпосередньо

## Обумовлені константи

**`UI\Controls\Box::Vertical`**

**`UI\Controls\Box::Horizontal`**

## Зміст

-   [UI\\Controls\\Box::append](ui-controls-box.append.html) — Додати елемент керування
-   [UI\\Controls\\Box::\_\_construct](ui-controls-box.construct.html) - Створити новий об'єкт Box
-   [UI\\Controls\\Box::delete](ui-controls-box.delete.html) — Видалити елемент керування
-   [UI\\Controls\\Box::getOrientation](ui-controls-box.getorientation.html) — Здобути орієнтацію
-   [UI\\Controls\\Box::isPadded](ui-controls-box.ispadded.html) - Визначення заповнення
-   [UI\\Controls\\Box::setPadded](ui-controls-box.setpadded.html) - Встановити заповнення