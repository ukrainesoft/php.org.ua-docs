---
navigation:
  - ui-point.sety.md: '« UIPoint::setY'
  - ui-size.construct.md: 'ОЙSize::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: 'Представляє розміри (ширина, висота)'
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

-   [ОЙSize::construct](ui-size.construct.md) — Створити новий об'єкт Size
-   [ОЙSize::getHeight](ui-size.getheight.md) — Отримує висоту
-   [ОЙSize::getWidth](ui-size.getwidth.md) — Отримує ширину
-   [ОЙSize::of](ui-size.of.md) - Приведення Point
-   [ОЙSize::setHeight](ui-size.setheight.md) - Встановити висоту
-   [ОЙSize::setWidth](ui-size.setwidth.md) - Встановити ширину
