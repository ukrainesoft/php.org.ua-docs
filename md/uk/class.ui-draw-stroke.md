Малювання обведення

-   [« UI\\Draw\\Color::setChannel](ui-draw-color.setchannel.html)
    
-   [UI\\Draw\\Stroke::\_\_construct »](ui-draw-stroke.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Малювання обведення
    

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

-   [UI\\Draw\\Stroke::\_\_construct](ui-draw-stroke.construct.html) - Створити новий об'єкт Stroke
-   [UI\\Draw\\Stroke::getCap](ui-draw-stroke.getcap.html) - Отримати кінець лінії
-   [UI\\Draw\\Stroke::getJoin](ui-draw-stroke.getjoin.html) — Отримати з'єднання лінії
-   [UI\\Draw\\Stroke::getMiterLimit](ui-draw-stroke.getmiterlimit.html) — Отримати межу зрізу
-   [UI\\Draw\\Stroke::getThickness](ui-draw-stroke.getthickness.html) - Отримати товщину
-   [UI\\Draw\\Stroke::setCap](ui-draw-stroke.setcap.html) - Встановити кінець лінії
-   [UI\\Draw\\Stroke::setJoin](ui-draw-stroke.setjoin.html) — Отримати з'єднання лінії
-   [UI\\Draw\\Stroke::setMiterLimit](ui-draw-stroke.setmiterlimit.html) - Встановити межу зрізу
-   [UI\\Draw\\Stroke::setThickness](ui-draw-stroke.setthickness.html) - Встановити товщину