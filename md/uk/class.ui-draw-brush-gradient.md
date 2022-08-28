Градієнтні пензлі

-   [« UI\\Draw\\Brush::setColor](ui-draw-brush.setcolor.html)
    
-   [UI\\Draw\\Brush\\Gradient::addStop »](ui-draw-brush-gradient.addstop.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Градієнтні пензлі
    

# Градієнтні пензлі

(UI 2.0.0)

## Вступ

Анотація клас для градієнтних пензлів

## Огляд класів

```classsynopsis



    
     
      abstract
      class UI\Draw\Brush\Gradient
     

     
      extends
       UI\Draw\Brush
     
     {


    /* Методы */
    
   public addStop(float $position, UI\Draw\Color $color): int
public addStop(float $position, int $color): int
public delStop(int $index): int
public setStop(int $index, float $position, UI\Draw\Color $color): bool
public setStop(int $index, float $position, int $color): bool


    /* Наследуемые методы */
    public UI\Draw\Brush::getColor(): UI\Draw\Color
public UI\Draw\Brush::setColor(UI\Draw\Color $color): void
public UI\Draw\Brush::setColor(int $color): void


   }
```

## Зміст

-   [UI\\Draw\\Brush\\Gradient::addStop](ui-draw-brush-gradient.addstop.html) - Додає вузол градієнта
-   [UI\\Draw\\Brush\\Gradient::delStop](ui-draw-brush-gradient.delstop.html) - Видаляє вузол градієнта
-   [UI\\Draw\\Brush\\Gradient::setStop](ui-draw-brush-gradient.setstop.html) - Встановлює вузол градієнта