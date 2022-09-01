---
navigation:
  - imagick.writeimagesfile.md: '« Imagick::writeImagesFile'
  - imagickdraw.affine.md: 'ImagickDraw::affine »'
  - index.md: PHP Manual
  - book.imagick.md: ImageMagick
title: 'Клас [ImagickDraw](class.imagickdraw.md)'
---
# Клас [ImagickDraw](class.imagickdraw.md)

(PECL imagick 2, PECL imagick 3)

## Огляд класів

```classsynopsis

    
     class ImagickDraw
     {
    
   public affine(array $affine): bool
public annotation(float $x, float $y, string $text): bool
public arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): bool
public bezier(array $coordinates): bool
public circle(    float $ox,    float $oy,    float $px,    float $py): bool
public clear(): bool
public clone(): ImagickDraw
public color(float $x, float $y, int $paintMethod): bool
public comment(string $comment): bool
public composite(    int $compose,    float $x,    float $y,    float $width,    float $height,    Imagick $compositeWand): bool
public __construct()
public destroy(): bool
public ellipse(    float $ox,    float $oy,    float $rx,    float $ry,    float $start,    float $end): bool
public getClipPath(): string
public getClipRule(): int
public getClipUnits(): int
public getFillColor(): ImagickPixel
public getFillOpacity(): float
public getFillRule(): int
public getFont(): string
public getFontFamily(): string
public getFontSize(): float
public getFontStretch(): int
public getFontStyle(): int
public getFontWeight(): int
public getGravity(): int
public getStrokeAntialias(): bool
public getStrokeColor(): ImagickPixel
public getStrokeDashArray(): array
public getStrokeDashOffset(): float
public getStrokeLineCap(): int
public getStrokeLineJoin(): int
public getStrokeMiterLimit(): int
public getStrokeOpacity(): float
public getStrokeWidth(): float
public getTextAlignment(): int
public getTextAntialias(): bool
public getTextDecoration(): int
public getTextEncoding(): string
public getTextInterlineSpacing(): float
public getTextInterwordSpacing(): float
public getTextKerning(): float
public getTextUnderColor(): ImagickPixel
public getVectorGraphics(): string
public line(    float $sx,    float $sy,    float $ex,    float $ey): bool
public matte(float $x, float $y, int $paintMethod): bool
public pathClose(): bool
public pathCurveToAbsolute(    float $x1,    float $y1,    float $x2,    float $y2,    float $x,    float $y): bool
public pathCurveToQuadraticBezierAbsolute(    float $x1,    float $y1,    float $x,    float $y): bool
public pathCurveToQuadraticBezierRelative(    float $x1,    float $y1,    float $x,    float $y): bool
public pathCurveToQuadraticBezierSmoothAbsolute(float $x, float $y): bool
public pathCurveToQuadraticBezierSmoothRelative(float $x, float $y): bool
public pathCurveToRelative(    float $x1,    float $y1,    float $x2,    float $y2,    float $x,    float $y): bool
public pathCurveToSmoothAbsolute(    float $x2,    float $y2,    float $x,    float $y): bool
public pathCurveToSmoothRelative(    float $x2,    float $y2,    float $x,    float $y): bool
public pathEllipticArcAbsolute(    float $rx,    float $ry,    float $x_axis_rotation,    bool $large_arc_flag,    bool $sweep_flag,    float $x,    float $y): bool
public pathEllipticArcRelative(    float $rx,    float $ry,    float $x_axis_rotation,    bool $large_arc_flag,    bool $sweep_flag,    float $x,    float $y): bool
public pathFinish(): bool
public pathLineToAbsolute(float $x, float $y): bool
public pathLineToHorizontalAbsolute(float $x): bool
public pathLineToHorizontalRelative(float $x): bool
public pathLineToRelative(float $x, float $y): bool
public pathLineToVerticalAbsolute(float $y): bool
public pathLineToVerticalRelative(float $y): bool
public pathMoveToAbsolute(float $x, float $y): bool
public pathMoveToRelative(float $x, float $y): bool
public pathStart(): bool
public point(float $x, float $y): bool
public polygon(array $coordinates): bool
public polyline(array $coordinates): bool
public pop(): bool
public popClipPath(): bool
public popDefs(): bool
public popPattern(): bool
public push(): bool
public pushClipPath(string $clip_mask_id): bool
public pushDefs(): bool
public pushPattern(    string $pattern_id,    float $x,    float $y,    float $width,    float $height): bool
public rectangle(    float $x1,    float $y1,    float $x2,    float $y2): bool
public render(): bool
public resetVectorGraphics(): bool
public rotate(float $degrees): bool
public roundRectangle(    float $x1,    float $y1,    float $x2,    float $y2,    float $rx,    float $ry): bool
public scale(float $x, float $y): bool
public setClipPath(string $clip_mask): bool
public setClipRule(int $fill_rule): bool
public setClipUnits(int $clip_units): bool
public setFillAlpha(float $opacity): bool
public setFillColor(ImagickPixel $fill_pixel): bool
public setFillOpacity(float $fillOpacity): bool
public setFillPatternURL(string $fill_url): bool
public setFillRule(int $fill_rule): bool
public setFont(string $font_name): bool
public setFontFamily(string $font_family): bool
public setFontSize(float $pointsize): bool
public setFontStretch(int $fontStretch): bool
public setFontStyle(int $style): bool
public setFontWeight(int $font_weight): bool
public setGravity(int $gravity): bool
public setResolution(float $x_resolution, float $y_resolution): bool
public setStrokeAlpha(float $opacity): bool
public setStrokeAntialias(bool $stroke_antialias): bool
public setStrokeColor(ImagickPixel $stroke_pixel): bool
public setStrokeDashArray(array $dashArray): bool
public setStrokeDashOffset(float $dash_offset): bool
public setStrokeLineCap(int $linecap): bool
public setStrokeLineJoin(int $linejoin): bool
public setStrokeMiterLimit(int $miterlimit): bool
public setStrokeOpacity(float $stroke_opacity): bool
public setStrokePatternURL(string $stroke_url): bool
public setStrokeWidth(float $stroke_width): bool
public setTextAlignment(int $alignment): bool
public setTextAntialias(bool $antiAlias): bool
public setTextDecoration(int $decoration): bool
public setTextEncoding(string $encoding): bool
public setTextInterlineSpacing(float $spacing): bool
public setTextInterwordSpacing(float $spacing): bool
public setTextKerning(float $kerning): bool
public setTextUnderColor(ImagickPixel $under_color): bool
public setVectorGraphics(string $xml): bool
public setViewbox(    int $x1,    int $y1,    int $x2,    int $y2): bool
public skewX(float $degrees): bool
public skewY(float $degrees): bool
public translate(float $x, float $y): bool

   }
```

## Зміст

-   [ImagickDraw::affine](imagickdraw.affine.md) - Регулює поточну матрицю афінного перетворення
-   [ImagickDraw::annotation](imagickdraw.annotation.md) — Малює текст на зображенні
-   [ImagickDraw::arc](imagickdraw.arc.md) — Малює дугу
-   [ImagickDraw::bezier](imagickdraw.bezier.md) — Малює криву Безьє
-   [ImagickDraw::circle](imagickdraw.circle.md) — Малює коло
-   [ImagickDraw::clear](imagickdraw.clear.md) - Очищає ImagickDraw
-   [ImagickDraw::clone](imagickdraw.clone.md) — Робить точну копію вказаного об'єкту ImagickDraw
-   [ImagickDraw::color](imagickdraw.color.md) — Малює колір на зображенні
-   [ImagickDraw::comment](imagickdraw.comment.md) — Додає коментар
-   [ImagickDraw::composite](imagickdraw.composite.md) — Накладає зображення на поточне зображення
-   [ImagickDraw::construct](imagickdraw.construct.md) - Конструктор класу ImagickDraw
-   [ImagickDraw::destroy](imagickdraw.destroy.md) — Звільняє усі пов'язані ресурси
-   [ImagickDraw::ellipse](imagickdraw.ellipse.md) — Малює на зображенні еліпс
-   [ImagickDraw::getClipPath](imagickdraw.getclippath.md) — Повертає ідентифікатор поточного відсічного контуру
-   [ImagickDraw::getClipRule](imagickdraw.getcliprule.md) — Повертає поточне правило заливання багатокутника
-   [ImagickDraw::getClipUnits](imagickdraw.getclipunits.md) — Повертає інтерпретацію одиниць відсічного контуру
-   [ImagickDraw::getFillColor](imagickdraw.getfillcolor.md) - Повертає колір заливки
-   [ImagickDraw::getFillOpacity](imagickdraw.getfillopacity.md) — Повертає непрозорість, яка використовується при малюванні.
-   [ImagickDraw::getFillRule](imagickdraw.getfillrule.md) — Повертає правило заливання
-   [ImagickDraw::getFont](imagickdraw.getfont.md) - Повертає шрифт
-   [ImagickDraw::getFontFamily](imagickdraw.getfontfamily.md) — Повертає сімейство шрифтів
-   [ImagickDraw::getFontSize](imagickdraw.getfontsize.md) — Повертає розмір шрифту
-   [ImagickDraw::getFontStretch](imagickdraw.getfontstretch.md) - Опис
-   [ImagickDraw::getFontStyle](imagickdraw.getfontstyle.md) — Повертає стиль шрифту
-   [ImagickDraw::getFontWeight](imagickdraw.getfontweight.md) — Повертає товщину шрифту
-   [ImagickDraw::getGravity](imagickdraw.getgravity.md) — Повертає гравітацію розміщення тексту
-   [ImagickDraw::getStrokeAntialias](imagickdraw.getstrokeantialias.md) — Повертає поточне налаштування згладжування обведення
-   [ImagickDraw::getStrokeColor](imagickdraw.getstrokecolor.md) — Повертає колір для обведення контурів об'єкта.
-   [ImagickDraw::getStrokeDashArray](imagickdraw.getstrokedasharray.md) — Повертає масив, що представляє патерн із штрихів та пробілів, які використовуються для обведення контурів.
-   [ImagickDraw::getStrokeDashOffset](imagickdraw.getstrokedashoffset.md) — Повертає зміщення у штриховому патерні для початку штрихування
-   [ImagickDraw::getStrokeLineCap](imagickdraw.getstrokelinecap.md) — Повертає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення
-   [ImagickDraw::getStrokeLineJoin](imagickdraw.getstrokelinejoin.md) — Повертає форму, яка використовуватиметься в кутах контурів під час їх обведення
-   [ImagickDraw::getStrokeMiterLimit](imagickdraw.getstrokemiterlimit.md) — Повертає межу зрізу обведення
-   [ImagickDraw::getStrokeOpacity](imagickdraw.getstrokeopacity.md) — Повертає непрозорість обведених контурів об'єкту
-   [ImagickDraw::getStrokeWidth](imagickdraw.getstrokewidth.md) — Повертає ширину обведення, яка використовується для малювання контурів об'єкта.
-   [ImagickDraw::getTextAlignment](imagickdraw.gettextalignment.md) — Повертає вирівнювання тексту
-   [ImagickDraw::getTextAntialias](imagickdraw.gettextantialias.md) — Повертає поточне налаштування згладжування тексту
-   [ImagickDraw::getTextDecoration](imagickdraw.gettextdecoration.md) — Повертає оформлення тексту
-   [ImagickDraw::getTextEncoding](imagickdraw.gettextencoding.md) — Повертає кодовий набір для текстових анотацій.
-   [ImagickDraw::getTextInterlineSpacing](imagickdraw.gettextinterlinespacing.md) — Повертає міжрядковий інтервал тексту
-   [ImagickDraw::getTextInterwordSpacing](imagickdraw.gettextinterwordspacing.md) — Повертає міжмовний інтервал тексту
-   [ImagickDraw::getTextKerning](imagickdraw.gettextkerning.md) — Повертає міжлітерний інтервал тексту
-   [ImagickDraw::getTextUnderColor](imagickdraw.gettextundercolor.md) — Повертає колір під текстом
-   [ImagickDraw::getVectorGraphics](imagickdraw.getvectorgraphics.md) — Повертає рядок, що містить векторну графіку
-   [ImagickDraw::line](imagickdraw.line.md) — Малює лінію
-   [ImagickDraw::matte](imagickdraw.matte.md) — Зафарбовує канал непрозорості зображення
-   [ImagickDraw::pathClose](imagickdraw.pathclose.md) — Додає елемент шляху до поточного шляху
-   [ImagickDraw::pathCurveToAbsolute](imagickdraw.pathcurvetoabsolute.md) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierAbsolute](imagickdraw.pathcurvetoquadraticbezierabsolute.md) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierRelative](imagickdraw.pathcurvetoquadraticbezierrelative.md) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierSmoothAbsolute](imagickdraw.pathcurvetoquadraticbeziersmoothabsolute.md) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierSmoothRelative](imagickdraw.pathcurvetoquadraticbeziersmoothrelative.md) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToRelative](imagickdraw.pathcurvetorelative.md) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToSmoothAbsolute](imagickdraw.pathcurvetosmoothabsolute.md) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToSmoothRelative](imagickdraw.pathcurvetosmoothrelative.md) — Малює кубічну криву Безьє
-   [ImagickDraw::pathEllipticArcAbsolute](imagickdraw.pathellipticarcabsolute.md) — Малює еліптичну дугу
-   [ImagickDraw::pathEllipticArcRelative](imagickdraw.pathellipticarcrelative.md) — Малює еліптичну дугу
-   [ImagickDraw::pathFinish](imagickdraw.pathfinish.md) - Завершує поточний шлях
-   [ImagickDraw::pathLineToAbsolute](imagickdraw.pathlinetoabsolute.md) — Малює лінію
-   [ImagickDraw::pathLineToHorizontalAbsolute](imagickdraw.pathlinetohorizontalabsolute.md) — Малює горизонтальну лінію
-   [ImagickDraw::pathLineToHorizontalRelative](imagickdraw.pathlinetohorizontalrelative.md) — Малює горизонтальну лінію
-   [ImagickDraw::pathLineToRelative](imagickdraw.pathlinetorelative.md) — Малює лінію
-   [ImagickDraw::pathLineToVerticalAbsolute](imagickdraw.pathlinetoverticalabsolute.md) — Малює вертикальну лінію
-   [ImagickDraw::pathLineToVerticalRelative](imagickdraw.pathlinetoverticalrelative.md) — Малює вертикальну лінію
-   [ImagickDraw::pathMoveToAbsolute](imagickdraw.pathmovetoabsolute.md) — Починає новий внутрішній контур
-   [ImagickDraw::pathMoveToRelative](imagickdraw.pathmovetorelative.md) — Починає новий внутрішній контур
-   [ImagickDraw::pathStart](imagickdraw.pathstart.md) — Оголошує початок відображення контуру
-   [ImagickDraw::point](imagickdraw.point.md) — Малює крапку
-   [ImagickDraw::polygon](imagickdraw.polygon.md) — Малює багатокутник
-   [ImagickDraw::polyline](imagickdraw.polyline.md) — Малює ламану лінію
-   [ImagickDraw::pop](imagickdraw.pop.md) — Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw
-   [ImagickDraw::popClipPath](imagickdraw.popclippath.md) — Завершує визначення шляху відсічного контуру
-   [ImagickDraw::popDefs](imagickdraw.popdefs.md) - Завершує список визначень
-   [ImagickDraw::popPattern](imagickdraw.poppattern.md) — Завершує визначення шаблону
-   [ImagickDraw::push](imagickdraw.push.md) — Клонує поточний об'єкт ImagickDraw і додає його до стек
-   [ImagickDraw::pushClipPath](imagickdraw.pushclippath.md) — Запускає визначення шляху відсічного контуру
-   [ImagickDraw::pushDefs](imagickdraw.pushdefs.md) - Вказує, що наступні команди створюють іменовані елементи для ранньої обробки
-   [ImagickDraw::pushPattern](imagickdraw.pushpattern.md) - Вказує, що наступні команди аж до ImagickDraw::opPattern() складають визначення іменованого патерну
-   [ImagickDraw::rectangle](imagickdraw.rectangle.md) — Малює прямокутник
-   [ImagickDraw::render](imagickdraw.render.md) — Малює всі попередні команди малювання на зображенні
-   [ImagickDraw::resetVectorGraphics](imagickdraw.resetvectorgraphics.md) — Скидає векторну графіку
-   [ImagickDraw::rotate](imagickdraw.rotate.md) — Застосовує зазначений поворот до поточного координатного простору
-   [ImagickDraw::roundRectangle](imagickdraw.roundrectangle.md) — Малює прямокутник із закругленими кутами.
-   [ImagickDraw::scale](imagickdraw.scale.md) - Регулює коефіцієнт масштабування
-   [ImagickDraw::setClipPath](imagickdraw.setclippath.md) — Зв'язує іменований контур відсічного контуру із зображенням
-   [ImagickDraw::setClipRule](imagickdraw.setcliprule.md) — Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур.
-   [ImagickDraw::setClipUnits](imagickdraw.setclipunits.md) — Встановлює інтерпретацію одиниць траєкторії відсічного контуру.
-   [ImagickDraw::setFillAlpha](imagickdraw.setfillalpha.md) — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.
-   [ImagickDraw::setFillColor](imagickdraw.setfillcolor.md) — Встановлює колір заливки для малювання об'єктів із заливкою.
-   [ImagickDraw::setFillOpacity](imagickdraw.setfillopacity.md) — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.
-   [ImagickDraw::setFillPatternURL](imagickdraw.setfillpatternurl.md) — Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів
-   [ImagickDraw::setFillRule](imagickdraw.setfillrule.md) — Встановлює правило заливання для використання під час малювання полігонів.
-   [ImagickDraw::setFont](imagickdraw.setfont.md) — Встановлює вказаний шрифт для використання під час анотування текстом
-   [ImagickDraw::setFontFamily](imagickdraw.setfontfamily.md) — Встановлює сімейство шрифтів для використання під час анотування текстом
-   [ImagickDraw::setFontSize](imagickdraw.setfontsize.md) — Встановлює розмір шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontStretch](imagickdraw.setfontstretch.md) — Встановлює розтягування шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontStyle](imagickdraw.setfontstyle.md) — Встановлює стиль шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontWeight](imagickdraw.setfontweight.md) — Встановлює товщину шрифту
-   [ImagickDraw::setGravity](imagickdraw.setgravity.md) - Встановлює гравітацію розміщення тексту
-   [ImagickDraw::setResolution](imagickdraw.setresolution.md) - Встановлює дозвіл
-   [ImagickDraw::setStrokeAlpha](imagickdraw.setstrokealpha.md) — Визначає непрозорість обведення контурів об'єкта
-   [ImagickDraw::setStrokeAntialias](imagickdraw.setstrokeantialias.md) — Керує згладжуванням обведення контурів
-   [ImagickDraw::setStrokeColor](imagickdraw.setstrokecolor.md) — Встановлює колір для обведення контурів об'єкта.
-   [ImagickDraw::setStrokeDashArray](imagickdraw.setstrokedasharray.md) — Задає патерн із штрихів та пробілів, які використовуються для обведення контурів.
-   [ImagickDraw::setStrokeDashOffset](imagickdraw.setstrokedashoffset.md) — Задає зміщення у штриховому патерні для початку штрихування
-   [ImagickDraw::setStrokeLineCap](imagickdraw.setstrokelinecap.md) — Задає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення
-   [ImagickDraw::setStrokeLineJoin](imagickdraw.setstrokelinejoin.md) — Задає форму, яка використовуватиметься в кутах контурів під час їх обведення
-   [ImagickDraw::setStrokeMiterLimit](imagickdraw.setstrokemiterlimit.md) - Задає межу зрізу обведення
-   [ImagickDraw::setStrokeOpacity](imagickdraw.setstrokeopacity.md) — Визначає непрозорість обведення контурів об'єкта
-   [ImagickDraw::setStrokePatternURL](imagickdraw.setstrokepatternurl.md) — Встановлює патерн для обведення контурів об'єкта.
-   [ImagickDraw::setStrokeWidth](imagickdraw.setstrokewidth.md) — Встановлює ширину обведення, яка використовується для малювання контурів об'єкта.
-   [ImagickDraw::setTextAlignment](imagickdraw.settextalignment.md) — Задає вирівнювання тексту
-   [ImagickDraw::setTextAntialias](imagickdraw.settextantialias.md) — керує згладжуванням тексту
-   [ImagickDraw::setTextDecoration](imagickdraw.settextdecoration.md) - Визначає оформлення
-   [ImagickDraw::setTextEncoding](imagickdraw.settextencoding.md) — Задає кодовий набір тексту
-   [ImagickDraw::setTextInterlineSpacing](imagickdraw.settextinterlinespacing.md) — Встановлює міжрядковий інтервал тексту
-   [ImagickDraw::setTextInterwordSpacing](imagickdraw.settextinterwordspacing.md) — Встановлює міжмовний інтервал тексту
-   [ImagickDraw::setTextKerning](imagickdraw.settextkerning.md) — Встановлює міжлітерний інтервал тексту
-   [ImagickDraw::setTextUnderColor](imagickdraw.settextundercolor.md) — Задає колір прямокутника фону
-   [ImagickDraw::setVectorGraphics](imagickdraw.setvectorgraphics.md) — Встановлює векторну графіку
-   [ImagickDraw::setViewbox](imagickdraw.setviewbox.md) - Встановлює загальний розмір полотна
-   [ImagickDraw::skewX](imagickdraw.skewx.md) - Нахиляє поточну систему координат по горизонталі.
-   [ImagickDraw::skewY](imagickdraw.skewy.md) - Нахиляє поточну систему координат по вертикалі
-   [ImagickDraw::translate](imagickdraw.translate.md) — Застосовує перенесення до поточної системи координат
