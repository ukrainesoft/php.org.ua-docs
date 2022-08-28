Шлях малювання

-   [« UI\\Draw\\Pen::write](ui-draw-pen.write.html)
    
-   [UI\\Draw\\Path::addRectangle »](ui-draw-path.addrectangle.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   Шлях малювання
    

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

-   [UI\\Draw\\Path::addRectangle](ui-draw-path.addrectangle.html) — Намалювати прямокутник
-   [UI\\Draw\\Path::arcTo](ui-draw-path.arcto.html) - Намалювати дугу
-   [UI\\Draw\\Path::bezierTo](ui-draw-path.bezierto.html) — Намалювати криву Безьє
-   [UI\\Draw\\Path::closeFigure](ui-draw-path.closefigure.html) - Закрити фігуру
-   [UI\\Draw\\Path::\_\_construct](ui-draw-path.construct.html) - Створити новий об'єкт Path
-   [UI\\Draw\\Path::end](ui-draw-path.end.html) - Завершити шлях
-   [UI\\Draw\\Path::lineTo](ui-draw-path.lineto.html) - Намалювати лінію
-   [UI\\Draw\\Path::newFigure](ui-draw-path.newfigure.html) — Намалювати фігуру
-   [UI\\Draw\\Path::newFigureWithArc](ui-draw-path.newfigurewitharc.html) - Намалювати фігуру з дугою