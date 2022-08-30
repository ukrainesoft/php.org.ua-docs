Представляє розміри (ширина, висота)

-   [« UIPoint::setY](ui-point.sety.html)
    
-   [ОЙSize::construct »](ui-size.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Представляє розміри (ширина, висота)
    

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

-   [ОЙSize::construct](ui-size.construct.html) — Створити новий об'єкт Size
-   [ОЙSize::getHeight](ui-size.getheight.html) — Отримує висоту
-   [ОЙSize::getWidth](ui-size.getwidth.html) — Отримує ширину
-   [ОЙSize::of](ui-size.of.html) - Приведення Point
-   [ОЙSize::setHeight](ui-size.setheight.html) - Встановити висоту
-   [ОЙSize::setWidth](ui-size.setwidth.html) - Встановити ширину