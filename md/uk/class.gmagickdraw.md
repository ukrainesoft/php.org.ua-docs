---
navigation:
  - gmagick.writeimage.md: '« Gmagick::writeimage'
  - gmagickdraw.annotate.md: 'GmagickDraw::annotate »'
  - index.md: PHP Manual
  - book.gmagick.md: Gmagick
title: Клас GmagickDraw
---
# Клас GmagickDraw

(PECL gmagick >= Unknown)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class GmagickDraw
     
     {
    

    /* Методы */
    
   public annotate(float $x, float $y, string $text): GmagickDraw
public arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): GmagickDraw
public bezier(array $coordinate_array): GmagickDraw
public ellipse(    float $ox,    float $oy,    float $rx,    float $ry,    float $start,    float $end): GmagickDraw
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
public line(    float $sx,    float $sy,    float $ex,    float $ey): GmagickDraw
public point(float $x, float $y): GmagickDraw
public polygon(array $coordinates): GmagickDraw
public polyline(array $coordinate_array): GmagickDraw
public rectangle(    float $x1,    float $y1,    float $x2,    float $y2): GmagickDraw
public rotate(float $degrees): GmagickDraw
public roundrectangle(    float $x1,    float $y1,    float $x2,    float $y2,    float $rx,    float $ry): GmagickDraw
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

-   [GmagickDraw::annotate](gmagickdraw.annotate.md) — Малює текст на зображенні
-   [GmagickDraw::arc](gmagickdraw.arc.md) — Малює дугу
-   [GmagickDraw::bezier](gmagickdraw.bezier.md) — Малює криву Безьє
-   [GmagickDraw::ellipse](gmagickdraw.ellipse.md) — Малює еліпс на зображенні
-   [GmagickDraw::getfillcolor](gmagickdraw.getfillcolor.md) - Повертає колір заливки
-   [GmagickDraw::getfillopacity](gmagickdraw.getfillopacity.md) — Повертає значення прозорості, що використовується під час малювання.
-   [GmagickDraw::getfont](gmagickdraw.getfont.md) - Повертає шрифт
-   [GmagickDraw::getfontsize](gmagickdraw.getfontsize.md) — Повертає розмір шрифту
-   [GmagickDraw::getfontstyle](gmagickdraw.getfontstyle.md) — Повертає стиль шрифту
-   [GmagickDraw::getfontweight](gmagickdraw.getfontweight.md) — Повертає товщину шрифту
-   [GmagickDraw::getstrokecolor](gmagickdraw.getstrokecolor.md) — Повертає колір для обведення контурів об'єкта.
-   [GmagickDraw::getstrokeopacity](gmagickdraw.getstrokeopacity.md) — Повертає прозорість обведених контурів об'єкта
-   [GmagickDraw::getstrokewidth](gmagickdraw.getstrokewidth.md) — Повертає ширину обведення, що використовується для відображення контурів об'єкта.
-   [GmagickDraw::gettextdecoration](gmagickdraw.gettextdecoration.md) — Повертає оформлення тексту
-   [GmagickDraw::gettextencoding](gmagickdraw.gettextencoding.md) — Повертає кодовий набір для текстових анотацій.
-   [GmagickDraw::line](gmagickdraw.line.md) — Малює лінію
-   [GmagickDraw::point](gmagickdraw.point.md) — Малює крапку
-   [GmagickDraw::polygon](gmagickdraw.polygon.md) — Малює багатокутник
-   [GmagickDraw::polyline](gmagickdraw.polyline.md) — Малює ламану лінію
-   [GmagickDraw::rectangle](gmagickdraw.rectangle.md) — Малює прямокутник
-   [GmagickDraw::rotate](gmagickdraw.rotate.md) — Застосовує зазначений поворот до поточного координатного простору
-   [GmagickDraw::roundrectangle](gmagickdraw.roundrectangle.md) — Малює прямокутник із закругленими кутами.
-   [GmagickDraw::scale](gmagickdraw.scale.md) - Регулює коефіцієнт масштабування
-   [GmagickDraw::setfillcolor](gmagickdraw.setfillcolor.md) — Встановлює колір заливки, який використовуватиметься для малювання об'єктів із заливкою
-   [GmagickDraw::setfillopacity](gmagickdraw.setfillopacity.md) - Встановлює непрозорість заливки
-   [GmagickDraw::setfont](gmagickdraw.setfont.md) — Встановлює вказаний шрифт для використання під час анотації тексту
-   [GmagickDraw::setfontsize](gmagickdraw.setfontsize.md) — Встановлює розмір шрифту для використання під час анотації тексту
-   [GmagickDraw::setfontstyle](gmagickdraw.setfontstyle.md) — Встановлює стиль шрифту для використання під час анотації тексту
-   [GmagickDraw::setfontweight](gmagickdraw.setfontweight.md) — Встановлює товщину шрифту
-   [GmagickDraw::setstrokecolor](gmagickdraw.setstrokecolor.md) — Встановлює колір для обведення контурів об'єкта.
-   [GmagickDraw::setstrokeopacity](gmagickdraw.setstrokeopacity.md) — Визначає прозорість обведення контурів об'єкта
-   [GmagickDraw::setstrokewidth](gmagickdraw.setstrokewidth.md) — Встановлює ширину обведення, що використовується для відображення контурів об'єкта.
-   [GmagickDraw::settextdecoration](gmagickdraw.settextdecoration.md) - Визначає оформлення
-   [GmagickDraw::settextencoding](gmagickdraw.settextencoding.md) — Задає кодовий набір тексту
