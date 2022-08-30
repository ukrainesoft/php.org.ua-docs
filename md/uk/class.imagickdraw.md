Клас ImagickDraw

-   [« Imagick::writeImagesFile](imagick.writeimagesfile.html)
    
-   [ImagickDraw::affine »](imagickdraw.affine.html)
    
-   [PHP Manual](index.html)
    
-   [ImageMagick](book.imagick.html)
    
-   Клас ImagickDraw
    

# Клас [ImagickDraw](class.imagickdraw.html)

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

-   [ImagickDraw::affine](imagickdraw.affine.html) - Регулює поточну матрицю афінного перетворення
-   [ImagickDraw::annotation](imagickdraw.annotation.html) — Малює текст на зображенні
-   [ImagickDraw::arc](imagickdraw.arc.html) — Малює дугу
-   [ImagickDraw::bezier](imagickdraw.bezier.html) — Малює криву Безьє
-   [ImagickDraw::circle](imagickdraw.circle.html) — Малює коло
-   [ImagickDraw::clear](imagickdraw.clear.html) - Очищає ImagickDraw
-   [ImagickDraw::clone](imagickdraw.clone.html) — Робить точну копію вказаного об'єкту ImagickDraw
-   [ImagickDraw::color](imagickdraw.color.html) — Малює колір на зображенні
-   [ImagickDraw::comment](imagickdraw.comment.html) — Додає коментар
-   [ImagickDraw::composite](imagickdraw.composite.html) — Накладає зображення на поточне зображення
-   [ImagickDraw::construct](imagickdraw.construct.html) - Конструктор класу ImagickDraw
-   [ImagickDraw::destroy](imagickdraw.destroy.html) — Звільняє усі пов'язані ресурси
-   [ImagickDraw::ellipse](imagickdraw.ellipse.html) — Малює на зображенні еліпс
-   [ImagickDraw::getClipPath](imagickdraw.getclippath.html) — Повертає ідентифікатор поточного відсічного контуру
-   [ImagickDraw::getClipRule](imagickdraw.getcliprule.html) — Повертає поточне правило заливання багатокутника
-   [ImagickDraw::getClipUnits](imagickdraw.getclipunits.html) — Повертає інтерпретацію одиниць відсічного контуру
-   [ImagickDraw::getFillColor](imagickdraw.getfillcolor.html) - Повертає колір заливки
-   [ImagickDraw::getFillOpacity](imagickdraw.getfillopacity.html) — Повертає непрозорість, яка використовується при малюванні.
-   [ImagickDraw::getFillRule](imagickdraw.getfillrule.html) — Повертає правило заливання
-   [ImagickDraw::getFont](imagickdraw.getfont.html) - Повертає шрифт
-   [ImagickDraw::getFontFamily](imagickdraw.getfontfamily.html) — Повертає сімейство шрифтів
-   [ImagickDraw::getFontSize](imagickdraw.getfontsize.html) — Повертає розмір шрифту
-   [ImagickDraw::getFontStretch](imagickdraw.getfontstretch.html) - Опис
-   [ImagickDraw::getFontStyle](imagickdraw.getfontstyle.html) — Повертає стиль шрифту
-   [ImagickDraw::getFontWeight](imagickdraw.getfontweight.html) — Повертає товщину шрифту
-   [ImagickDraw::getGravity](imagickdraw.getgravity.html) — Повертає гравітацію розміщення тексту
-   [ImagickDraw::getStrokeAntialias](imagickdraw.getstrokeantialias.html) — Повертає поточне налаштування згладжування обведення
-   [ImagickDraw::getStrokeColor](imagickdraw.getstrokecolor.html) — Повертає колір для обведення контурів об'єкта.
-   [ImagickDraw::getStrokeDashArray](imagickdraw.getstrokedasharray.html) — Повертає масив, що представляє патерн із штрихів та пробілів, які використовуються для обведення контурів.
-   [ImagickDraw::getStrokeDashOffset](imagickdraw.getstrokedashoffset.html) — Повертає зміщення у штриховому патерні для початку штрихування
-   [ImagickDraw::getStrokeLineCap](imagickdraw.getstrokelinecap.html) — Повертає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення
-   [ImagickDraw::getStrokeLineJoin](imagickdraw.getstrokelinejoin.html) — Повертає форму, яка використовуватиметься в кутах контурів під час їх обведення
-   [ImagickDraw::getStrokeMiterLimit](imagickdraw.getstrokemiterlimit.html) — Повертає межу зрізу обведення
-   [ImagickDraw::getStrokeOpacity](imagickdraw.getstrokeopacity.html) — Повертає непрозорість обведених контурів об'єкту
-   [ImagickDraw::getStrokeWidth](imagickdraw.getstrokewidth.html) — Повертає ширину обведення, яка використовується для малювання контурів об'єкта.
-   [ImagickDraw::getTextAlignment](imagickdraw.gettextalignment.html) — Повертає вирівнювання тексту
-   [ImagickDraw::getTextAntialias](imagickdraw.gettextantialias.html) — Повертає поточне налаштування згладжування тексту
-   [ImagickDraw::getTextDecoration](imagickdraw.gettextdecoration.html) — Повертає оформлення тексту
-   [ImagickDraw::getTextEncoding](imagickdraw.gettextencoding.html) — Повертає кодовий набір для текстових анотацій.
-   [ImagickDraw::getTextInterlineSpacing](imagickdraw.gettextinterlinespacing.html) — Повертає міжрядковий інтервал тексту
-   [ImagickDraw::getTextInterwordSpacing](imagickdraw.gettextinterwordspacing.html) — Повертає міжмовний інтервал тексту
-   [ImagickDraw::getTextKerning](imagickdraw.gettextkerning.html) — Повертає міжлітерний інтервал тексту
-   [ImagickDraw::getTextUnderColor](imagickdraw.gettextundercolor.html) — Повертає колір під текстом
-   [ImagickDraw::getVectorGraphics](imagickdraw.getvectorgraphics.html) — Повертає рядок, що містить векторну графіку
-   [ImagickDraw::line](imagickdraw.line.html) — Малює лінію
-   [ImagickDraw::matte](imagickdraw.matte.html) — Зафарбовує канал непрозорості зображення
-   [ImagickDraw::pathClose](imagickdraw.pathclose.html) — Додає елемент шляху до поточного шляху
-   [ImagickDraw::pathCurveToAbsolute](imagickdraw.pathcurvetoabsolute.html) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierAbsolute](imagickdraw.pathcurvetoquadraticbezierabsolute.html) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierRelative](imagickdraw.pathcurvetoquadraticbezierrelative.html) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierSmoothAbsolute](imagickdraw.pathcurvetoquadraticbeziersmoothabsolute.html) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToQuadraticBezierSmoothRelative](imagickdraw.pathcurvetoquadraticbeziersmoothrelative.html) — Малює квадратичну криву Безьє
-   [ImagickDraw::pathCurveToRelative](imagickdraw.pathcurvetorelative.html) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToSmoothAbsolute](imagickdraw.pathcurvetosmoothabsolute.html) — Малює кубічну криву Безьє
-   [ImagickDraw::pathCurveToSmoothRelative](imagickdraw.pathcurvetosmoothrelative.html) — Малює кубічну криву Безьє
-   [ImagickDraw::pathEllipticArcAbsolute](imagickdraw.pathellipticarcabsolute.html) — Малює еліптичну дугу
-   [ImagickDraw::pathEllipticArcRelative](imagickdraw.pathellipticarcrelative.html) — Малює еліптичну дугу
-   [ImagickDraw::pathFinish](imagickdraw.pathfinish.html) - Завершує поточний шлях
-   [ImagickDraw::pathLineToAbsolute](imagickdraw.pathlinetoabsolute.html) — Малює лінію
-   [ImagickDraw::pathLineToHorizontalAbsolute](imagickdraw.pathlinetohorizontalabsolute.html) — Малює горизонтальну лінію
-   [ImagickDraw::pathLineToHorizontalRelative](imagickdraw.pathlinetohorizontalrelative.html) — Малює горизонтальну лінію
-   [ImagickDraw::pathLineToRelative](imagickdraw.pathlinetorelative.html) — Малює лінію
-   [ImagickDraw::pathLineToVerticalAbsolute](imagickdraw.pathlinetoverticalabsolute.html) — Малює вертикальну лінію
-   [ImagickDraw::pathLineToVerticalRelative](imagickdraw.pathlinetoverticalrelative.html) — Малює вертикальну лінію
-   [ImagickDraw::pathMoveToAbsolute](imagickdraw.pathmovetoabsolute.html) — Починає новий внутрішній контур
-   [ImagickDraw::pathMoveToRelative](imagickdraw.pathmovetorelative.html) — Починає новий внутрішній контур
-   [ImagickDraw::pathStart](imagickdraw.pathstart.html) — Оголошує початок відображення контуру
-   [ImagickDraw::point](imagickdraw.point.html) — Малює крапку
-   [ImagickDraw::polygon](imagickdraw.polygon.html) — Малює багатокутник
-   [ImagickDraw::polyline](imagickdraw.polyline.html) — Малює ламану лінію
-   [ImagickDraw::pop](imagickdraw.pop.html) — Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw
-   [ImagickDraw::popClipPath](imagickdraw.popclippath.html) — Завершує визначення шляху відсічного контуру
-   [ImagickDraw::popDefs](imagickdraw.popdefs.html) - Завершує список визначень
-   [ImagickDraw::popPattern](imagickdraw.poppattern.html) — Завершує визначення шаблону
-   [ImagickDraw::push](imagickdraw.push.html) — Клонує поточний об'єкт ImagickDraw і додає його до стек
-   [ImagickDraw::pushClipPath](imagickdraw.pushclippath.html) — Запускає визначення шляху відсічного контуру
-   [ImagickDraw::pushDefs](imagickdraw.pushdefs.html) - Вказує, що наступні команди створюють іменовані елементи для ранньої обробки
-   [ImagickDraw::pushPattern](imagickdraw.pushpattern.html) - Вказує, що наступні команди аж до ImagickDraw::opPattern() складають визначення іменованого патерну
-   [ImagickDraw::rectangle](imagickdraw.rectangle.html) — Малює прямокутник
-   [ImagickDraw::render](imagickdraw.render.html) — Малює всі попередні команди малювання на зображенні
-   [ImagickDraw::resetVectorGraphics](imagickdraw.resetvectorgraphics.html) — Скидає векторну графіку
-   [ImagickDraw::rotate](imagickdraw.rotate.html) — Застосовує зазначений поворот до поточного координатного простору
-   [ImagickDraw::roundRectangle](imagickdraw.roundrectangle.html) — Малює прямокутник із закругленими кутами.
-   [ImagickDraw::scale](imagickdraw.scale.html) - Регулює коефіцієнт масштабування
-   [ImagickDraw::setClipPath](imagickdraw.setclippath.html) — Зв'язує іменований контур відсічного контуру із зображенням
-   [ImagickDraw::setClipRule](imagickdraw.setcliprule.html) — Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур.
-   [ImagickDraw::setClipUnits](imagickdraw.setclipunits.html) — Встановлює інтерпретацію одиниць траєкторії відсічного контуру.
-   [ImagickDraw::setFillAlpha](imagickdraw.setfillalpha.html) — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.
-   [ImagickDraw::setFillColor](imagickdraw.setfillcolor.html) — Встановлює колір заливки для малювання об'єктів із заливкою.
-   [ImagickDraw::setFillOpacity](imagickdraw.setfillopacity.html) — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.
-   [ImagickDraw::setFillPatternURL](imagickdraw.setfillpatternurl.html) — Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів
-   [ImagickDraw::setFillRule](imagickdraw.setfillrule.html) — Встановлює правило заливання для використання під час малювання полігонів.
-   [ImagickDraw::setFont](imagickdraw.setfont.html) — Встановлює вказаний шрифт для використання під час анотування текстом
-   [ImagickDraw::setFontFamily](imagickdraw.setfontfamily.html) — Встановлює сімейство шрифтів для використання під час анотування текстом
-   [ImagickDraw::setFontSize](imagickdraw.setfontsize.html) — Встановлює розмір шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontStretch](imagickdraw.setfontstretch.html) — Встановлює розтягування шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontStyle](imagickdraw.setfontstyle.html) — Встановлює стиль шрифту для використання під час анотування текстом
-   [ImagickDraw::setFontWeight](imagickdraw.setfontweight.html) — Встановлює товщину шрифту
-   [ImagickDraw::setGravity](imagickdraw.setgravity.html) - Встановлює гравітацію розміщення тексту
-   [ImagickDraw::setResolution](imagickdraw.setresolution.html) - Встановлює дозвіл
-   [ImagickDraw::setStrokeAlpha](imagickdraw.setstrokealpha.html) — Визначає непрозорість обведення контурів об'єкта
-   [ImagickDraw::setStrokeAntialias](imagickdraw.setstrokeantialias.html) — Керує згладжуванням обведення контурів
-   [ImagickDraw::setStrokeColor](imagickdraw.setstrokecolor.html) — Встановлює колір для обведення контурів об'єкта.
-   [ImagickDraw::setStrokeDashArray](imagickdraw.setstrokedasharray.html) — Задає патерн із штрихів та пробілів, які використовуються для обведення контурів.
-   [ImagickDraw::setStrokeDashOffset](imagickdraw.setstrokedashoffset.html) — Задає зміщення у штриховому патерні для початку штрихування
-   [ImagickDraw::setStrokeLineCap](imagickdraw.setstrokelinecap.html) — Задає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення
-   [ImagickDraw::setStrokeLineJoin](imagickdraw.setstrokelinejoin.html) — Задає форму, яка використовуватиметься в кутах контурів під час їх обведення
-   [ImagickDraw::setStrokeMiterLimit](imagickdraw.setstrokemiterlimit.html) - Задає межу зрізу обведення
-   [ImagickDraw::setStrokeOpacity](imagickdraw.setstrokeopacity.html) — Визначає непрозорість обведення контурів об'єкта
-   [ImagickDraw::setStrokePatternURL](imagickdraw.setstrokepatternurl.html) — Встановлює патерн для обведення контурів об'єкта.
-   [ImagickDraw::setStrokeWidth](imagickdraw.setstrokewidth.html) — Встановлює ширину обведення, яка використовується для малювання контурів об'єкта.
-   [ImagickDraw::setTextAlignment](imagickdraw.settextalignment.html) — Задає вирівнювання тексту
-   [ImagickDraw::setTextAntialias](imagickdraw.settextantialias.html) — керує згладжуванням тексту
-   [ImagickDraw::setTextDecoration](imagickdraw.settextdecoration.html) - Визначає оформлення
-   [ImagickDraw::setTextEncoding](imagickdraw.settextencoding.html) — Задає кодовий набір тексту
-   [ImagickDraw::setTextInterlineSpacing](imagickdraw.settextinterlinespacing.html) — Встановлює міжрядковий інтервал тексту
-   [ImagickDraw::setTextInterwordSpacing](imagickdraw.settextinterwordspacing.html) — Встановлює міжмовний інтервал тексту
-   [ImagickDraw::setTextKerning](imagickdraw.settextkerning.html) — Встановлює міжлітерний інтервал тексту
-   [ImagickDraw::setTextUnderColor](imagickdraw.settextundercolor.html) — Задає колір прямокутника фону
-   [ImagickDraw::setVectorGraphics](imagickdraw.setvectorgraphics.html) — Встановлює векторну графіку
-   [ImagickDraw::setViewbox](imagickdraw.setviewbox.html) - Встановлює загальний розмір полотна
-   [ImagickDraw::skewX](imagickdraw.skewx.html) - Нахиляє поточну систему координат по горизонталі.
-   [ImagickDraw::skewY](imagickdraw.skewy.html) - Нахиляє поточну систему координат по вертикалі
-   [ImagickDraw::translate](imagickdraw.translate.html) — Застосовує перенесення до поточної системи координат