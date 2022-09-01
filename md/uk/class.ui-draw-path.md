---
navigation:
  - ui-draw-pen.write.html: '« UIDrawPen::write'
  - ui-draw-path.addrectangle.html: 'ОЙDrawPath::addRectangle »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Шлях малювання
---
# Шлях малювання

(UI 0.9.9)

## Вступ

Шлях малювання спрямовує перо, де малювати по області

## Огляд класів

```classsynopsis



    
     
      class UI\Draw\Path
     
     {

    /* Константы */
    
     const
     int
      Winding;

    const
     int
      Alternate;


    /* Конструктор */
    
   public __construct(int $mode = UI\Draw\Path::Winding)


    /* Методы */
    public addRectangle(UI\Point $point, UI\Size $size)
public arcTo(    UI\Point $point,    float $radius,    float $angle,    float $sweep,    float $negative)
public bezierTo(    UI\Point $point,    float $radius,    float $angle,    float $sweep,    float $negative)
public closeFigure()
public end()
public lineTo(    UI\Point $point,    float $radius,    float $angle,    float $sweep,    float $negative)
public newFigure(UI\Point $point)
public newFigureWithArc(    UI\Point $point,    float $radius,    float $angle,    float $sweep,    float $negative)

   }
```

## Обумовлені константи

**`UI\Draw\Path::Winding`**

Це режим малювання за умовчанням

**`UI\Draw\Path::Alternate`**

Це альтернативний режим малювання

## Зміст

-   [ОЙDrawPath::addRectangle](ui-draw-path.addrectangle.html) — Намалювати прямокутник
-   [ОЙDrawPath::arcTo](ui-draw-path.arcto.html) - Намалювати дугу
-   [ОЙDrawPath::bezierTo](ui-draw-path.bezierto.html) — Намалювати криву Безьє
-   [ОЙDrawPath::closeFigure](ui-draw-path.closefigure.html) - Закрити фігуру
-   [ОЙDrawPath::construct](ui-draw-path.construct.html) - Створити новий об'єкт Path
-   [ОЙDrawPath::end](ui-draw-path.end.html) - Завершити шлях
-   [ОЙDrawPath::lineTo](ui-draw-path.lineto.html) - Намалювати лінію
-   [ОЙDrawPath::newFigure](ui-draw-path.newfigure.html) — Намалювати фігуру
-   [ОЙDrawPath::newFigureWithArc](ui-draw-path.newfigurewitharc.html) - Намалювати фігуру з дугою
