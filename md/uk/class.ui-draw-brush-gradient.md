---
navigation:
  - ui-draw-brush.setcolor.html: '« UIDrawBrush::setColor'
  - ui-draw-brush-gradient.addstop.html: 'ОЙDrawBrushGradient::addStop »'
  - index.html: PHP Manual
  - book.ui.html: ОЙ
title: Градієнтні пензлі
---
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

-   [ОЙDrawBrushGradient::addStop](ui-draw-brush-gradient.addstop.md) - Додає вузол градієнта
-   [ОЙDrawBrushGradient::delStop](ui-draw-brush-gradient.delstop.md) - Видаляє вузол градієнта
-   [ОЙDrawBrushGradient::setStop](ui-draw-brush-gradient.setstop.md) - Встановлює вузол градієнта
