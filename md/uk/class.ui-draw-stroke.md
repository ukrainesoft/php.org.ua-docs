---
navigation:
  - ui-draw-color.setchannel.md: '« UIDrawColor::setChannel'
  - ui-draw-stroke.construct.md: 'ОЙDrawStroke::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Малювання обведення
---
# Малювання обведення

(UI 0.9.9)

## Вступ

Містить конфігурацію Pen для виконання обведення

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Stroke
     
     {


    /* Конструктор */
    
   public __construct(    int $cap = UI\Draw\Line\Cap::Flat,    int $join = UI\Draw\Line\Join::Miter,    float $thickness = 1,    float $miterLimit = 10)


    /* Методы */
    public getCap(): int
public getJoin(): int
public getMiterLimit(): float
public getThickness(): float
public setCap(int $cap)
public setJoin(int $join)
public setMiterLimit(float $limit)
public setThickness(float $thickness)

   }
```

## Зміст

-   [ОЙDrawStroke::construct](ui-draw-stroke.construct.md) - Створити новий об'єкт Stroke
-   [ОЙDrawStroke::getCap](ui-draw-stroke.getcap.md) - Отримати кінець лінії
-   [ОЙDrawStroke::getJoin](ui-draw-stroke.getjoin.md) — Отримати з'єднання лінії
-   [ОЙDrawStroke::getMiterLimit](ui-draw-stroke.getmiterlimit.md) — Отримати межу зрізу
-   [ОЙDrawStroke::getThickness](ui-draw-stroke.getthickness.md) - Отримати товщину
-   [ОЙDrawStroke::setCap](ui-draw-stroke.setcap.md) - Встановити кінець лінії
-   [ОЙDrawStroke::setJoin](ui-draw-stroke.setjoin.md) — Отримати з'єднання лінії
-   [ОЙDrawStroke::setMiterLimit](ui-draw-stroke.setmiterlimit.md) - Встановити межу зрізу
-   [ОЙDrawStroke::setThickness](ui-draw-stroke.setthickness.md) - Встановити товщину
