---
navigation:
  - ui-point.sety.md: '« UI\\Point::setY'
  - ui-size.construct.md: 'UI\\Size::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: 'Представляє розміри (ширина, висота)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Представляє розміри (ширина, висота)

(UI 0.9.9)

## Вступ

Розміри використовуються в інтерфейсі користувача для представлення розміру екрана, керуючого елемента або області.

## Огляд класів

```classsynopsis



    
     
      final
      class UI\Size
     
     {

    /* Свойства */
    
     public
      $width;

    public
      $height;


    /* Конструктор */
    
   public __construct(float $width, float $height)


    /* Методы */
    public getHeight(): float
public getWidth(): float
public static of(float $size): UI\Size
public static of(UI\Point $point): UI\Size
public setHeight(float $size)
public setWidth(float $size)

   }
```

## Властивості

width

Містить ширину, може бути прочитана/записана безпосередньо

height

Містить висоту, може бути прочитана/записана безпосередньо

## Зміст

-   [UI\\Size::\_\_construct](ui-size.construct.md)— Створити новий об'єкт Size
-   [UI\\Size::getHeight](ui-size.getheight.md)— Отримує висоту
-   [UI\\Size::getWidth](ui-size.getwidth.md)— Отримує ширину
-   [UI\\Size::of](ui-size.of.md) \- Приведення Point
-   [UI\\Size::setHeight](ui-size.setheight.md) \- Встановити висоту
-   [UI\\Size::setWidth](ui-size.setwidth.md) \- Встановити ширину
