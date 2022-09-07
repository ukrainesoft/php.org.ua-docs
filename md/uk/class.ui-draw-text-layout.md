---
navigation:
  - ui-draw-brush-radialgradient.construct.md: '« UIDrawBrushRadialGradient::construct'
  - ui-draw-text-layout.construct.md: 'ОЙDrawTextLayout::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Представляє макет тексту
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

-   [ОЙDrawTextLayout::construct](ui-draw-text-layout.construct.md) — Створити новий об'єкт макету тексту
-   [ОЙDrawTextLayout::setColor](ui-draw-text-layout.setcolor.md) - Встановити колір
-   [ОЙDrawTextLayout::setWidth](ui-draw-text-layout.setwidth.md) - Встановити ширину
