Представляє позицію (x, y)

-   [« Установка](ui.installation.html)
    
-   [UI\\Point::at »](ui-point.at.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Представляє позицію (x, y)
    

# Представляє позицію (x, y)

(UI 0.9.9)

## Вступ

Точки використовуються у всьому інтерфейсі користувача для представлення координат на екрані, керуючому елементі або області.

## Огляд класів

```classsynopsis



    
     
      final
      class UI\Point
     
     {

    /* Свойства */
    
     public
      $x;

    public
      $y;


    /* Конструктор */
    
   public __construct(float $x, float $y)


    /* Методы */
    public static at(float $point): UI\Point
public static at(UI\Size $size): UI\Point
public getX(): float
public getY(): float
public setX(float $point)
public setY(float $point)

   }
```

## Властивості

з

Містить координату X, може бути прочитана/записана безпосередньо

і

Містить координату Y, може бути прочитана/записана безпосередньо

## Зміст

-   [UI\\Point::at](ui-point.at.html) - Приведення Size
-   [UI\\Point::\_\_construct](ui-point.construct.html) — Створити новий об'єкт Point
-   [UI\\Point::getX](ui-point.getx.html) — Отримує X
-   [UI\\Point::getY](ui-point.gety.html) - Отримати Y
-   [UI\\Point::setX](ui-point.setx.html) - Встановити X
-   [UI\\Point::setY](ui-point.sety.html) - Встановити Y