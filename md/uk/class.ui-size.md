Представляє розміри (ширина, висота)

-   [« UI\\Point::setY](ui-point.sety.html)
    
-   [UI\\Size::\_\_construct »](ui-size.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
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

-   [UI\\Size::\_\_construct](ui-size.construct.html) — Створити новий об'єкт Size
-   [UI\\Size::getHeight](ui-size.getheight.html) — Отримує висоту
-   [UI\\Size::getWidth](ui-size.getwidth.html) — Отримує ширину
-   [UI\\Size::of](ui-size.of.html) - Приведення Point
-   [UI\\Size::setHeight](ui-size.setheight.html) - Встановити висоту
-   [UI\\Size::setWidth](ui-size.setwidth.html) - Встановити ширину