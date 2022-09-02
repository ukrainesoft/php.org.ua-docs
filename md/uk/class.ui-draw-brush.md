---
navigation:
  - ui-draw-stroke.setthickness.md: '« UIDrawStroke::setThickness'
  - ui-draw-brush.construct.md: 'ОЙDrawBrush::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Щітки
---
# Щітки

(UI 0.9.9)

## Вступ

Представляє суцільний кольоровий пензель

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Brush
     
     {


    /* Конструктор */
    
   public __construct(UI\Draw\Color $color)
public __construct(int $color)


    /* Методы */
    public getColor(): UI\Draw\Color
public setColor(UI\Draw\Color $color): void
public setColor(int $color): void

    }
```

## Зміст

-   [ОЙDrawBrush::construct](ui-draw-brush.construct.md) — Створити новий об'єкт Brush
-   [ОЙDrawBrush::getColor](ui-draw-brush.getcolor.md) - Отримати колір
-   [ОЙDrawBrush::setColor](ui-draw-brush.setcolor.md) - Встановити колір
