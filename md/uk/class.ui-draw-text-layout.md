---
navigation:
  - ui-draw-brush-radialgradient.construct.md: '« UI\\Draw\\Brush\\RadialGradient::\_\_construct'
  - ui-draw-text-layout.construct.md: 'UI\\Draw\\Text\\Layout::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Представляє макет тексту
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Представляє макет тексту

(UI 0.9.9)

## Вступ

Текстовий макет є макетом тексту, який буде намальований пером

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Text\Layout
     
     {


    /* Конструктор */
    
   public __construct(string $text, UI\Draw\Text\Font $font, float $width)


    /* Методы */
    public setColor(UI\Draw\Color $color, int $start = 0, int $end = ?)
public setColor(int $color, int $start = 0, int $end = ?)
public setWidth(float $width)

   }
```

## Зміст

-   [UI\\Draw\\Text\\Layout::\_\_construct](ui-draw-text-layout.construct.md)— Створити новий об'єкт макету тексту
-   [UI\\Draw\\Text\\Layout::setColor](ui-draw-text-layout.setcolor.md) \- Встановити колір
-   [UI\\Draw\\Text\\Layout::setWidth](ui-draw-text-layout.setwidth.md) \- Встановити ширину
