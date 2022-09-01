---
navigation:
  - ui-controls-group.settitle.html: '« UIControlsGroup::setTitle'
  - ui-controls-box.append.html: 'ОЙControlsBox::append »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Блок керування (розміщення)
---
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

-   [ОЙControlsBox::append](ui-controls-box.append.md) — Додати елемент керування
-   [ОЙControlsBox::construct](ui-controls-box.construct.md) - Створити новий об'єкт Box
-   [ОЙControlsBox::delete](ui-controls-box.delete.md) — Видалити елемент керування
-   [ОЙControlsBox::getOrientation](ui-controls-box.getorientation.md) — Здобути орієнтацію
-   [ОЙControlsBox::isPadded](ui-controls-box.ispadded.md) - Визначення заповнення
-   [ОЙControlsBox::setPadded](ui-controls-box.setpadded.md) - Встановити заповнення
