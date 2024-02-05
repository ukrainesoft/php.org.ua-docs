---
navigation:
  - ui-draw-brush-gradient.setstop.md: '« UI\\Draw\\Brush\\Gradient::setStop'
  - ui-draw-brush-lineargradient.construct.md: 'UI\\Draw\\Brush\\LinearGradient::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Лінійний градієнт
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Brush\\LinearGradient::\_\_construct](ui-draw-brush-lineargradient.construct.md) \- Конструктор класу LinearGradient
