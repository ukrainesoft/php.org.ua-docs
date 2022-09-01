---
navigation:
  - ui.installation.md: « Установка
  - ui-point.at.html: 'ОЙPoint::at »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: 'Представляє позицію (x, y)'
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

з

Містить координату X, може бути прочитана/записана безпосередньо

і

Містить координату Y, може бути прочитана/записана безпосередньо

## Зміст

-   [ОЙPoint::at](ui-point.at.md) - Приведення Size
-   [ОЙPoint::construct](ui-point.construct.md) — Створити новий об'єкт Point
-   [ОЙPoint::getX](ui-point.getx.md) — Отримує X
-   [ОЙPoint::getY](ui-point.gety.md) - Отримати Y
-   [ОЙPoint::setX](ui-point.setx.md) - Встановити X
-   [ОЙPoint::setY](ui-point.sety.md) - Встановити Y
