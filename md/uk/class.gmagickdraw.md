Клас GmagickDraw

-   [« Gmagick::writeimage](gmagick.writeimage.html)
    
-   [GmagickDraw::annotate »](gmagickdraw.annotate.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](book.gmagick.html)
    
-   Клас GmagickDraw
    

# Клас GmagickDraw

(PECL gmagick >= Unknown)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class GmagickDraw
     
     {
    

    /* Методы */
    
   public annotate(float $x, float $y, string $text): GmagickDraw
public arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): GmagickDraw
public bezier(array $coordinate_array): GmagickDraw
public ellipse(    float $ox,    float $oy,    float $rx,    float $ry,    float $start,    float $end): GmagickDraw
public getfillcolor(): GmagickPixel
public getfillopacity(): float
public getfont(): mixed
public getfontsize(): float
public getfontstyle(): int
public getfontweight(): int
public getstrokecolor(): GmagickPixel
public getstrokeopacity(): float
public getstrokewidth(): float
public gettextdecoration(): int
public gettextencoding(): mixed
public line(    float $sx,    float $sy,    float $ex,    float $ey): GmagickDraw
public point(float $x, float $y): GmagickDraw
public polygon(array $coordinates): GmagickDraw
public polyline(array $coordinate_array): GmagickDraw
public rectangle(    float $x1,    float $y1,    float $x2,    float $y2): GmagickDraw
public rotate(float $degrees): GmagickDraw
public roundrectangle(    float $x1,    float $y1,    float $x2,    float $y2,    float $rx,    float $ry): GmagickDraw
public scale(float $x, float $y): GmagickDraw
public setfillcolor(mixed $color): GmagickDraw
public setfillopacity(float $fill_opacity): GmagickDraw
public setfont(string $font): GmagickDraw
public setfontsize(float $pointsize): GmagickDraw
public setfontstyle(int $style): GmagickDraw
public setfontweight(int $weight): GmagickDraw
public setstrokecolor(mixed $color): GmagickDraw
public setstrokeopacity(float $stroke_opacity): GmagickDraw
public setstrokewidth(float $width): GmagickDraw
public settextdecoration(int $decoration): GmagickDraw
public settextencoding(string $encoding): GmagickDraw

   }
```

## Зміст

-   [GmagickDraw::annotate](gmagickdraw.annotate.html) — Малює текст на зображенні
-   [GmagickDraw::arc](gmagickdraw.arc.html) — Малює дугу
-   [GmagickDraw::bezier](gmagickdraw.bezier.html) — Малює криву Безьє
-   [GmagickDraw::ellipse](gmagickdraw.ellipse.html) — Малює еліпс на зображенні
-   [GmagickDraw::getfillcolor](gmagickdraw.getfillcolor.html) - Повертає колір заливки
-   [GmagickDraw::getfillopacity](gmagickdraw.getfillopacity.html) — Повертає значення прозорості, що використовується під час малювання.
-   [GmagickDraw::getfont](gmagickdraw.getfont.html) - Повертає шрифт
-   [GmagickDraw::getfontsize](gmagickdraw.getfontsize.html) — Повертає розмір шрифту
-   [GmagickDraw::getfontstyle](gmagickdraw.getfontstyle.html) — Повертає стиль шрифту
-   [GmagickDraw::getfontweight](gmagickdraw.getfontweight.html) — Повертає товщину шрифту
-   [GmagickDraw::getstrokecolor](gmagickdraw.getstrokecolor.html) — Повертає колір для обведення контурів об'єкта.
-   [GmagickDraw::getstrokeopacity](gmagickdraw.getstrokeopacity.html) — Повертає прозорість обведених контурів об'єкта
-   [GmagickDraw::getstrokewidth](gmagickdraw.getstrokewidth.html) — Повертає ширину обведення, що використовується для відображення контурів об'єкта.
-   [GmagickDraw::gettextdecoration](gmagickdraw.gettextdecoration.html) — Повертає оформлення тексту
-   [GmagickDraw::gettextencoding](gmagickdraw.gettextencoding.html) — Повертає кодовий набір для текстових анотацій.
-   [GmagickDraw::line](gmagickdraw.line.html) — Малює лінію
-   [GmagickDraw::point](gmagickdraw.point.html) — Малює крапку
-   [GmagickDraw::polygon](gmagickdraw.polygon.html) — Малює багатокутник
-   [GmagickDraw::polyline](gmagickdraw.polyline.html) — Малює ламану лінію
-   [GmagickDraw::rectangle](gmagickdraw.rectangle.html) — Малює прямокутник
-   [GmagickDraw::rotate](gmagickdraw.rotate.html) — Застосовує зазначений поворот до поточного координатного простору
-   [GmagickDraw::roundrectangle](gmagickdraw.roundrectangle.html) — Малює прямокутник із закругленими кутами.
-   [GmagickDraw::scale](gmagickdraw.scale.html) - Регулює коефіцієнт масштабування
-   [GmagickDraw::setfillcolor](gmagickdraw.setfillcolor.html) — Встановлює колір заливки, який використовуватиметься для малювання об'єктів із заливкою
-   [GmagickDraw::setfillopacity](gmagickdraw.setfillopacity.html) - Встановлює непрозорість заливки
-   [GmagickDraw::setfont](gmagickdraw.setfont.html) — Встановлює вказаний шрифт для використання під час анотації тексту
-   [GmagickDraw::setfontsize](gmagickdraw.setfontsize.html) — Встановлює розмір шрифту для використання під час анотації тексту
-   [GmagickDraw::setfontstyle](gmagickdraw.setfontstyle.html) — Встановлює стиль шрифту для використання під час анотації тексту
-   [GmagickDraw::setfontweight](gmagickdraw.setfontweight.html) — Встановлює товщину шрифту
-   [GmagickDraw::setstrokecolor](gmagickdraw.setstrokecolor.html) — Встановлює колір для обведення контурів об'єкта.
-   [GmagickDraw::setstrokeopacity](gmagickdraw.setstrokeopacity.html) — Визначає прозорість обведення контурів об'єкта
-   [GmagickDraw::setstrokewidth](gmagickdraw.setstrokewidth.html) — Встановлює ширину обведення, що використовується для відображення контурів об'єкта.
-   [GmagickDraw::settextdecoration](gmagickdraw.settextdecoration.html) - Визначає оформлення
-   [GmagickDraw::settextencoding](gmagickdraw.settextencoding.html) — Задає кодовий набір тексту