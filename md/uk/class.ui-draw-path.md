---
navigation:
  - ui-draw-pen.write.md: '« UI\\Draw\\Pen::write'
  - ui-draw-path.addrectangle.md: 'UI\\Draw\\Path::addRectangle »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Шлях малювання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Draw\\Path::addRectangle](ui-draw-path.addrectangle.md)— Намалювати прямокутник
-   [UI\\Draw\\Path::arcTo](ui-draw-path.arcto.md) \- Намалювати дугу
-   [UI\\Draw\\Path::bezierTo](ui-draw-path.bezierto.md)— Намалювати криву Безьє
-   [UI\\Draw\\Path::closeFigure](ui-draw-path.closefigure.md) \- Закрити фігуру
-   [UI\\Draw\\Path::\_\_construct](ui-draw-path.construct.md) \- Створити новий об'єкт Path
-   [UI\\Draw\\Path::end](ui-draw-path.end.md) \- Завершити шлях
-   [UI\\Draw\\Path::lineTo](ui-draw-path.lineto.md) \- Намалювати лінію
-   [UI\\Draw\\Path::newFigure](ui-draw-path.newfigure.md)— Намалювати фігуру
-   [UI\\Draw\\Path::newFigureWithArc](ui-draw-path.newfigurewitharc.md) \- Намалювати фігуру з дугою
