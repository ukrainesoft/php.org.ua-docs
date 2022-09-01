---
navigation:
  - ui-draw-brush-gradient.setstop.html: '« UIDrawBrushGradient::setStop'
  - ui-draw-brush-lineargradient.construct.html: 'ОЙDrawBrushLinearGradient::construct »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Лінійний градієнт
---
# Лінійний градієнт

(UI 2.0.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Brush\LinearGradient
     

     
      extends
       UI\Draw\Brush\Gradient
     
     {


    /* Конструктор */
    
   public __construct(UI\Point $start, UI\Point $end)


    

    /* Наследуемые методы */
    public UI\Draw\Brush\Gradient::addStop(float $position, UI\Draw\Color $color): int
public UI\Draw\Brush\Gradient::addStop(float $position, int $color): int
public UI\Draw\Brush\Gradient::delStop(int $index): int
public UI\Draw\Brush\Gradient::setStop(int $index, float $position, UI\Draw\Color $color): bool
public UI\Draw\Brush\Gradient::setStop(int $index, float $position, int $color): bool


   }
```

## Зміст

-   [ОЙDrawBrushLinearGradient::construct](ui-draw-brush-lineargradient.construct.html) - Конструктор класу LinearGradient
