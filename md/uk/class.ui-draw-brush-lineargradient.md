Лінійний градієнт

-   [« UI\\Draw\\Brush\\Gradient::setStop](ui-draw-brush-gradient.setstop.html)
    
-   [UI\\Draw\\Brush\\LinearGradient::\_\_construct »](ui-draw-brush-lineargradient.construct.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Лінійний градієнт
    

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

-   [UI\\Draw\\Brush\\LinearGradient::\_\_construct](ui-draw-brush-lineargradient.construct.html) - Конструктор класу LinearGradient