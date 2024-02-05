---
navigation:
  - ui-draw-brush.setcolor.md: '« UI\\Draw\\Brush::setColor'
  - ui-draw-brush-gradient.addstop.md: 'UI\\Draw\\Brush\\Gradient::addStop »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Градієнтні пензлі
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Brush\\Gradient::addStop](ui-draw-brush-gradient.addstop.md) \- Додає вузол градієнта
-   [UI\\Draw\\Brush\\Gradient::delStop](ui-draw-brush-gradient.delstop.md) \- Видаляє вузол градієнта
-   [UI\\Draw\\Brush\\Gradient::setStop](ui-draw-brush-gradient.setstop.md) \- Встановлює вузол градієнта
