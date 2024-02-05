---
navigation:
  - ui.installation.md: « Встановлення
  - ui-point.at.md: 'UI\\Point::at »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: 'Представляє позицію (x, y)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

x

Містить координату X, може бути прочитана/записана безпосередньо

y

Містить координату Y, може бути прочитана/записана безпосередньо

## Зміст

-   [UI\\Point::at](ui-point.at.md) \- Приведення Size
-   [UI\\Point::\_\_construct](ui-point.construct.md)— Створити новий об'єкт Point
-   [UI\\Point::getX](ui-point.getx.md)— Отримує X
-   [UI\\Point::getY](ui-point.gety.md) \- Отримати Y
-   [UI\\Point::setX](ui-point.setx.md) \- Встановити X
-   [UI\\Point::setY](ui-point.sety.md) \- Встановити Y
