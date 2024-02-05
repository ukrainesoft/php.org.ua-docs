---
navigation:
  - ui-draw-color.setchannel.md: '« UI\\Draw\\Color::setChannel'
  - ui-draw-stroke.construct.md: 'UI\\Draw\\Stroke::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Малювання обведення
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
    
   public __construct(    int $cap = UI\Draw\Line\Cap::Flat,    int $join = UI\Draw\Line\Join::Miter,    float $thickness = 1,    float $miterLimit = 10)


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

-   [UI\\Draw\\Stroke::\_\_construct](ui-draw-stroke.construct.md) \- Створити новий об'єкт Stroke
-   [UI\\Draw\\Stroke::getCap](ui-draw-stroke.getcap.md) \- Отримати кінець лінії
-   [UI\\Draw\\Stroke::getJoin](ui-draw-stroke.getjoin.md)— Отримати з'єднання лінії
-   [UI\\Draw\\Stroke::getMiterLimit](ui-draw-stroke.getmiterlimit.md)— Отримати межу зрізу
-   [UI\\Draw\\Stroke::getThickness](ui-draw-stroke.getthickness.md) \- Отримати товщину
-   [UI\\Draw\\Stroke::setCap](ui-draw-stroke.setcap.md) \- Встановити кінець лінії
-   [UI\\Draw\\Stroke::setJoin](ui-draw-stroke.setjoin.md)— Отримати з'єднання лінії
-   [UI\\Draw\\Stroke::setMiterLimit](ui-draw-stroke.setmiterlimit.md) \- Встановити межу зрізу
-   [UI\\Draw\\Stroke::setThickness](ui-draw-stroke.setthickness.md) \- Встановити товщину
