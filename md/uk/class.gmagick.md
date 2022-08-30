Клас Gmagick

-   [« Приклади](gmagick.examples.md)
    
-   [Gmagick::addimage »](gmagick.addimage.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](book.gmagick.md)
    
-   Клас Gmagick
    

# Клас Gmagick

(PECL gmagick >= Unknown)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Gmagick
     
     {
    
    /* Методы */
    
   public __construct(string $filename = ?)

    public addimage(Gmagick $source): Gmagick
public addnoiseimage(int $noise_type): Gmagick
public annotateimage(    GmagickDraw $GmagickDraw,    float $x,    float $y,    float $angle,    string $text): Gmagick
public blurimage(float $radius, float $sigma, int $channel = ?): Gmagick
public borderimage(GmagickPixel $color, int $width, int $height): Gmagick
public charcoalimage(float $radius, float $sigma): Gmagick
public chopimage(    int $width,    int $height,    int $x,    int $y): Gmagick
public clear(): Gmagick
public commentimage(string $comment): Gmagick
public compositeimage(    Gmagick $source,    int $COMPOSE,    int $x,    int $y): Gmagick
public cropimage(    
    int
     $width
   ,    
    int
     $height
   ,    int $x,    int $y): Gmagick
public cropthumbnailimage(int $width, int $height): Gmagick
public current(): Gmagick
public cyclecolormapimage(int $displace): Gmagick
public deconstructimages(): Gmagick
public despeckleimage(): Gmagick
public destroy(): bool
public drawimage(GmagickDraw $GmagickDraw): Gmagick
public edgeimage(float $radius): Gmagick
public embossimage(float $radius, float $sigma): Gmagick
public enhanceimage(): Gmagick
public equalizeimage(): Gmagick
public flipimage(): Gmagick
public flopimage(): Gmagick
public frameimage(    GmagickPixel $color,    int $width,    int $height,    int $inner_bevel,    int $outer_bevel): Gmagick
public gammaimage(float $gamma): Gmagick
public getcopyright(): string
public getfilename(): string
public getimagebackgroundcolor(): GmagickPixel
public getimageblueprimary(): array
public getimagebordercolor(): GmagickPixel
public getimagechanneldepth(int $channel_type): int
public getimagecolors(): int
public getimagecolorspace(): int
public getimagecompose(): int
public getimagedelay(): int
public getimagedepth(): int
public getimagedispose(): int
public getimageextrema(): array
public getimagefilename(): string
public getimageformat(): string
public getimagegamma(): float
public getimagegreenprimary(): array
public getimageheight(): int
public getimagehistogram(): array
public getimageindex(): int
public getimageinterlacescheme(): int
public getimageiterations(): int
public getimagematte(): int
public getimagemattecolor(): GmagickPixel
public getimageprofile(string $name): string
public getimageredprimary(): array
public getimagerenderingintent(): int
public getimageresolution(): array
public getimagescene(): int
public getimagesignature(): string
public getimagetype(): int
public getimageunits(): int
public getimagewhitepoint(): array
public getimagewidth(): int
public getpackagename(): string
public getquantumdepth(): array
public getreleasedate(): string
public getsamplingfactors(): array
public getsize(): array
public getversion(): array
public hasnextimage(): mixed
public haspreviousimage(): mixed
public implodeimage(float $radius): mixed
public labelimage(string $label): mixed
public levelimage(    float $blackPoint,    float $gamma,    float $whitePoint,    int $channel = Gmagick::CHANNEL_DEFAULT): mixed
public magnifyimage(): mixed
public mapimage(gmagick $gmagick, bool $dither): Gmagick
public medianfilterimage(float $radius): void
public minifyimage(): Gmagick
public modulateimage(float $brightness, float $saturation, float $hue): Gmagick
public motionblurimage(float $radius, float $sigma, float $angle): Gmagick
public newimage(    int $width,    int $height,    string $background,    string $format = ?): Gmagick
public nextimage(): bool
public normalizeimage(int $channel = ?): Gmagick
public oilpaintimage(
      float
       $radius
    ): Gmagick
public previousimage(): bool
public profileimage(string $name, string $profile): Gmagick
public quantizeimage(    int $numColors,    int $colorspace,    int $treeDepth,    bool $dither,    bool $measureError): Gmagick
public quantizeimages(    int $numColors,    int $colorspace,    int $treeDepth,    bool $dither,    bool $measureError): Gmagick
public queryfontmetrics(GmagickDraw $draw, string $text): array
public queryfonts(string $pattern = "*"): array
public queryformats(string $pattern = "*"): array
public radialblurimage(float $angle, int $channel = Gmagick::CHANNEL_DEFAULT): Gmagick
public raiseimage(    int $width,    int $height,    int $x,    int $y,    bool $raise): Gmagick
public read(string $filename): Gmagick
public readimage(string $filename): Gmagick
public readimageblob(string $imageContents, string $filename = ?): Gmagick
public readimagefile(resource $fp, string $filename = ?): Gmagick
public reducenoiseimage(float $radius): Gmagick
public removeimage(): Gmagick
public removeimageprofile(string $name): string
public resampleimage(    float $xResolution,    float $yResolution,    int $filter,    float $blur): Gmagick
public resizeimage(    int $width,    int $height,    int $filter,    float $blur,    bool $fit = false): Gmagick
public rollimage(int $x, int $y): Gmagick
public rotateimage(mixed $color, float $degrees): Gmagick
public scaleimage(int $width, int $height, bool $fit = false): Gmagick
public separateimagechannel(int $channel): Gmagick
setCompressionQuality(
    int $quality
     = 75
   ): Gmagick
public setfilename(string $filename): Gmagick
public setimagebackgroundcolor(GmagickPixel $color): Gmagick
public setimageblueprimary(float $x, float $y): Gmagick
public setimagebordercolor(GmagickPixel $color): Gmagick
public setimagechanneldepth(int $channel, int $depth): Gmagick
public setimagecolorspace(int $colorspace): Gmagick
public setimagecompose(int $composite): Gmagick
public setimagedelay(int $delay): Gmagick
public setimagedepth(int $depth): Gmagick
public setimagedispose(int $disposeType): Gmagick
public setimagefilename(string $filename): Gmagick
public setimageformat(string $imageFormat): Gmagick
public setimagegamma(float $gamma): Gmagick
public setimagegreenprimary(float $x, float $y): Gmagick
public setimageindex(int $index): Gmagick
public setimageinterlacescheme(int $interlace): Gmagick
public setimageiterations(int $iterations): Gmagick
public setimageprofile(string $name, string $profile): Gmagick
public setimageredprimary(float $x, float $y): Gmagick
public setimagerenderingintent(int $rendering_intent): Gmagick
public setimageresolution(float $xResolution, float $yResolution): Gmagick
public setimagescene(int $scene): Gmagick
public setimagetype(int $imgType): Gmagick
public setimageunits(int $resolution): Gmagick
public setimagewhitepoint(float $x, float $y): Gmagick
public setsamplingfactors(array $factors): Gmagick
public setsize(int $columns, int $rows): Gmagick
public shearimage(mixed $color, float $xShear, float $yShear): Gmagick
public solarizeimage(int $threshold): Gmagick
public spreadimage(float $radius): Gmagick
public stripimage(): Gmagick
public swirlimage(float $degrees): Gmagick
public thumbnailimage(int $width, int $height, bool $fit = false): Gmagick
public trimimage(float $fuzz): Gmagick
public writeimage(string $filename, bool $all_frames = false): Gmagick

   }
```

## Зміст

-   [Gmagick::addimage](gmagick.addimage.md) — Додавання нового зображення до списку зображень об'єкта Gmagick
-   [Gmagick::addnoiseimage](gmagick.addnoiseimage.md) — Додає випадкового шуму до зображення
-   [Gmagick::annotateimage](gmagick.annotateimage.md) — Підписати зображення текстом
-   [Gmagick::blurimage](gmagick.blurimage.md) — Додати розмиття зображення
-   [Gmagick::borderimage](gmagick.borderimage.md) — Додати рамку до зображення
-   [Gmagick::charcoalimage](gmagick.charcoalimage.md) — Імітація малювання вугіллям
-   [Gmagick::chopimage](gmagick.chopimage.md) — Видаляє область зображення та підрізає його.
-   [Gmagick::clear](gmagick.clear.md) — Зачищає всі ресурси, пов'язані з об'єктом Gmagick
-   [Gmagick::commentimage](gmagick.commentimage.md) — Додати коментар до зображення
-   [Gmagick::compositeimage](gmagick.compositeimage.md) — Накладає одне зображення на інше
-   [Gmagick::construct](gmagick.construct.md) - Конструктор об'єкта Gmagick
-   [Gmagick::cropimage](gmagick.cropimage.md) — Обрізає зображення
-   [Gmagick::cropthumbnailimage](gmagick.cropthumbnailimage.md) — Створення обрізаного зменшеного зображення
-   [Gmagick::current](gmagick.current.md) - Повернути самого себе
-   [Gmagick::cyclecolormapimage](gmagick.cyclecolormapimage.md) — Зміщує колірну карту зображення
-   [Gmagick::deconstructimages](gmagick.deconstructimages.md) — Повертає певні піксельні відмінності між зображеннями
-   [Gmagick::despeckleimage](gmagick.despeckleimage.md) - Призначення despeckleimage
-   [Gmagick::destroy](gmagick.destroy.md) — Знищити об'єкт Gmagick
-   [Gmagick::drawimage](gmagick.drawimage.md) — Відображає об'єкт GmagickDraw на поточному зображенні
-   [Gmagick::edgeimage](gmagick.edgeimage.md) — Збільшує краї зображення.
-   [Gmagick::embossimage](gmagick.embossimage.md) — Повертає зображення у градаціях сірого із тривимірним ефектом
-   [Gmagick::enhanceimage](gmagick.enhanceimage.md) — Покращує якість зображення із шумом
-   [Gmagick::equalizeimage](gmagick.equalizeimage.md) — Вирівнює гістограму зображення
-   [Gmagick::flipimage](gmagick.flipimage.md) — Створює вертикальне дзеркальне відображення
-   [Gmagick::flopimage](gmagick.flopimage.md) — Створює горизонтальне дзеркальне відображення
-   [Gmagick::frameimage](gmagick.frameimage.md) — Додає змодельований тривимірний кордон
-   [Gmagick::gammaimage](gmagick.gammaimage.md) - Гамма-корекція зображення
-   [Gmagick::getcopyright](gmagick.getcopyright.md) — Повертає копірайт GraphicsMagick API у вигляді рядка
-   [Gmagick::getfilename](gmagick.getfilename.md) — Повертає ім'я файлу, пов'язаного з послідовністю зображень.
-   [Gmagick::getimagebackgroundcolor](gmagick.getimagebackgroundcolor.md) — Повертає колір тла зображення
-   [Gmagick::getimageblueprimary](gmagick.getimageblueprimary.md) — Повертає кольоровість синьої первинної точки
-   [Gmagick::getimagebordercolor](gmagick.getimagebordercolor.md) — Повертає колір кордону зображення
-   [Gmagick::getimagechanneldepth](gmagick.getimagechanneldepth.md) — Отримує глибину для певного каналу зображення
-   [Gmagick::getimagecolors](gmagick.getimagecolors.md) — Повертає колір зазначеного індексу карти кольорів
-   [Gmagick::getimagecolorspace](gmagick.getimagecolorspace.md) — Повертає колірний простір зображення
-   [Gmagick::getimagecompose](gmagick.getimagecompose.md) — Повертає складовий оператор, пов'язаний із зображенням
-   [Gmagick::getimagedelay](gmagick.getimagedelay.md) — Отримує затримку зображення
-   [Gmagick::getimagedepth](gmagick.getimagedepth.md) — Отримує глибину зображення
-   [Gmagick::getimagedispose](gmagick.getimagedispose.md) — Отримує метод видалення зображення
-   [Gmagick::getimageextrema](gmagick.getimageextrema.md) — Отримує екстремуми для зображення
-   [Gmagick::getimagefilename](gmagick.getimagefilename.md) — Повертає ім'я файлу конкретного зображення у послідовності
-   [Gmagick::getimageformat](gmagick.getimageformat.md) — Повертає формат зображення в послідовності.
-   [Gmagick::getimagegamma](gmagick.getimagegamma.md) — Повертає гаму зображення
-   [Gmagick::getimagegreenprimary](gmagick.getimagegreenprimary.md) — Повертає первинну зелену точку
-   [Gmagick::getimageheight](gmagick.getimageheight.md) — Повертає висоту зображення
-   [Gmagick::getimagehistogram](gmagick.getimagehistogram.md) — Повертає гістограму зображення
-   [Gmagick::getimageindex](gmagick.getimageindex.md) — Повертає індекс активного поточного зображення.
-   [Gmagick::getimageinterlacescheme](gmagick.getimageinterlacescheme.md) — Отримує схему чергування зображень
-   [Gmagick::getimageiterations](gmagick.getimageiterations.md) — Отримує ітерацію зображення
-   [Gmagick::getimagematte](gmagick.getimagematte.md) — Перевіряє, чи є на зображенні матовий канал
-   [Gmagick::getimagemattecolor](gmagick.getimagemattecolor.md) — Повертає зображення матового кольору
-   [Gmagick::getimageprofile](gmagick.getimageprofile.md) — Повертає іменований профайл зображення
-   [Gmagick::getimageredprimary](gmagick.getimageredprimary.md) — Повертає первинну червону точку
-   [Gmagick::getimagerenderingintent](gmagick.getimagerenderingintent.md) — Отримує мету рендерингу зображення
-   [Gmagick::getimageresolution](gmagick.getimageresolution.md) — Повертає роздільну здатність зображення
-   [Gmagick::getimagescene](gmagick.getimagescene.md) — Отримує сцену зображення
-   [Gmagick::getimagesignature](gmagick.getimagesignature.md) — Створює підпис до повідомлення SHA-256
-   [Gmagick::getimagetype](gmagick.getimagetype.md) — Повертає потенційний тип зображення
-   [Gmagick::getimageunits](gmagick.getimageunits.md) — Повертає одиниці роздільної здатності зображення
-   [Gmagick::getimagewhitepoint](gmagick.getimagewhitepoint.md) — Повертає хроматичну білу крапку
-   [Gmagick::getimagewidth](gmagick.getimagewidth.md) — Повертає ширину зображення
-   [Gmagick::getpackagename](gmagick.getpackagename.md) — Повертає ім'я пакета GraphicsMagick
-   [Gmagick::getquantumdepth](gmagick.getquantumdepth.md) — Повертає глибину кольору (біт на канал) об'єкта Gmagick у вигляді рядка
-   [Gmagick::getreleasedate](gmagick.getreleasedate.md) — Повертає дату релізу GraphicsMagick у вигляді рядка
-   [Gmagick::getsamplingfactors](gmagick.getsamplingfactors.md) — Повертає вертикальний та горизонтальний фактор дискретизації
-   [Gmagick::getsize](gmagick.getsize.md) — Повертає розмір, пов'язаний із об'єктом Gmagick
-   [Gmagick::getversion](gmagick.getversion.md) — Повертає версію GraphicsMagick API
-   [Gmagick::hasnextimage](gmagick.hasnextimage.md) — Перевіряє, чи є ще зображення в об'єкті
-   [Gmagick::haspreviousimage](gmagick.haspreviousimage.md) — Перевіряє, чи є ще зображення в об'єкті під час ітерації назад
-   [Gmagick::implodeimage](gmagick.implodeimage.md) — Створює копію зображення
-   [Gmagick::labelimage](gmagick.labelimage.md) — Додає позначку до зображення
-   [Gmagick::levelimage](gmagick.levelimage.md) — Регулює рівні зображення
-   [Gmagick::magnifyimage](gmagick.magnifyimage.md) - Пропорційно масштабує зображення в 2 рази
-   [Gmagick::mapimage](gmagick.mapimage.md) — Замінює кольори зображення на найближчий колір із еталонного зображення
-   [Gmagick::medianfilterimage](gmagick.medianfilterimage.md) — Застосовує цифровий фільтр
-   [Gmagick::minifyimage](gmagick.minifyimage.md) — Масштабує зображення пропорційно до половини його розміру.
-   [Gmagick::modulateimage](gmagick.modulateimage.md) — Керує яскравістю, насиченістю та відтінком
-   [Gmagick::motionblurimage](gmagick.motionblurimage.md) — Імітує розмиття під час руху
-   [Gmagick::newimage](gmagick.newimage.md) — Створює нове зображення
-   [Gmagick::nextimage](gmagick.nextimage.md) — Здійснює перехід до наступного зображення
-   [Gmagick::normalizeimage](gmagick.normalizeimage.md) — Підвищує контрастність кольорового зображення
-   [Gmagick::oilpaintimage](gmagick.oilpaintimage.md) — Імітує ефект картини олією
-   [Gmagick::previousimage](gmagick.previousimage.md) — Здійснює перехід до попереднього зображення в об'єкті
-   [Gmagick::profileimage](gmagick.profileimage.md) — Додає або видаляє профіль із зображення.
-   [Gmagick::quantizeimage](gmagick.quantizeimage.md) - Аналізує кольори еталонного зображення
-   [Gmagick::quantizeimages](gmagick.quantizeimages.md) — Аналізує кольори у послідовності зображень
-   [Gmagick::queryfontmetrics](gmagick.queryfontmetrics.md) — Повертає масив, який представляє метрики шрифту
-   [Gmagick::queryfonts](gmagick.queryfonts.md) — Повертає налаштовані шрифти
-   [Gmagick::queryformats](gmagick.queryformats.md) — Повертає формати Gmagick.
-   [Gmagick::radialblurimage](gmagick.radialblurimage.md) — Застосовує радіальне розмиття зображення.
-   [Gmagick::raiseimage](gmagick.raiseimage.md) — Створює імітацію ефекту тривимірної кнопки
-   [Gmagick::read](gmagick.read.md) — Читає зображення із файлу
-   [Gmagick::readimage](gmagick.readimage.md) — Читає зображення із файлу
-   [Gmagick::readimageblob](gmagick.readimageblob.md) — Читає зображення з бінарного рядка
-   [Gmagick::readimagefile](gmagick.readimagefile.md) — Читає зображення або послідовність зображень із файлового дескриптора
-   [Gmagick::reducenoiseimage](gmagick.reducenoiseimage.md) — Згладжує контури зображення
-   [Gmagick::removeimage](gmagick.removeimage.md) — Видаляє зображення зі списку
-   [Gmagick::removeimageprofile](gmagick.removeimageprofile.md) — Видаляє іменований профайл зображення та повертає його
-   [Gmagick::resampleimage](gmagick.resampleimage.md) — Змінює роздільну здатність зображення до бажаного.
-   [Gmagick::resizeimage](gmagick.resizeimage.md) — Масштабує зображення
-   [Gmagick::rollimage](gmagick.rollimage.md) — Зміщує зображення
-   [Gmagick::rotateimage](gmagick.rotateimage.md) — Повертає зображення
-   [Gmagick::scaleimage](gmagick.scaleimage.md) — Масштабує розмір зображення
-   [Gmagick::separateimagechannel](gmagick.separateimagechannel.md) — Відокремлює канал від зображення.
-   [Gmagick::setCompressionQuality](gmagick.setcompressionquality.md) — Встановлює якість стандартного стиснення об'єкта
-   [Gmagick::setfilename](gmagick.setfilename.md) — Встановлює ім'я файлу перед читанням чи записом зображення
-   [Gmagick::setimagebackgroundcolor](gmagick.setimagebackgroundcolor.md) — Встановлює колір тла зображення
-   [Gmagick::setimageblueprimary](gmagick.setimageblueprimary.md) — Встановлює кольоровість зображення блакитною основною точкою.
-   [Gmagick::setimagebordercolor](gmagick.setimagebordercolor.md) — Встановлює колір рамки зображення
-   [Gmagick::setimagechanneldepth](gmagick.setimagechanneldepth.md) — Встановлює глибину певного каналу зображення
-   [Gmagick::setimagecolorspace](gmagick.setimagecolorspace.md) — Встановлює колірний простір зображення
-   [Gmagick::setimagecompose](gmagick.setimagecompose.md) — Встановлює оператор складеного зображення
-   [Gmagick::setimagedelay](gmagick.setimagedelay.md) — Встановлює затримку зображення
-   [Gmagick::setimagedepth](gmagick.setimagedepth.md) — Встановлює глибину зображення
-   [Gmagick::setimagedispose](gmagick.setimagedispose.md) — Встановлює метод видалення зображення
-   [Gmagick::setimagefilename](gmagick.setimagefilename.md) — Встановлює ім'я файлу конкретного зображення у послідовності
-   [Gmagick::setimageformat](gmagick.setimageformat.md) — Встановлює формат певного зображення
-   [Gmagick::setimagegamma](gmagick.setimagegamma.md) — Встановлює гаму зображення
-   [Gmagick::setimagegreenprimary](gmagick.setimagegreenprimary.md) — Встановлює кольоровість зображення зеленою первинною точкою.
-   [Gmagick::setimageindex](gmagick.setimageindex.md) — Встановлює ітератор у положення списку зображень, заданому параметром index
-   [Gmagick::setimageinterlacescheme](gmagick.setimageinterlacescheme.md) — Встановлює схему надстрокової розгортки зображення
-   [Gmagick::setimageiterations](gmagick.setimageiterations.md) — Встановлює ітерацію зображення
-   [Gmagick::setimageprofile](gmagick.setimageprofile.md) — Додає іменований профіль до об'єкту Gmagick
-   [Gmagick::setimageredprimary](gmagick.setimageredprimary.md) — Встановлює кольоровість зображення червоною основною точкою.
-   [Gmagick::setimagerenderingintent](gmagick.setimagerenderingintent.md) — Встановлює спосіб рендерингу зображення
-   [Gmagick::setimageresolution](gmagick.setimageresolution.md) — Встановлює роздільну здатність зображення
-   [Gmagick::setimagescene](gmagick.setimagescene.md) — Встановлює сцену зображення
-   [Gmagick::setimagetype](gmagick.setimagetype.md) — Встановлює тип зображення
-   [Gmagick::setimageunits](gmagick.setimageunits.md) — Встановлює одиниці роздільної здатності зображення
-   [Gmagick::setimagewhitepoint](gmagick.setimagewhitepoint.md) — Встановлює кольоровість зображення білою точкою.
-   [Gmagick::setsamplingfactors](gmagick.setsamplingfactors.md) — Встановлює фактори вибірки зображення
-   [Gmagick::setsize](gmagick.setsize.md) — Встановлює розмір об'єкта Gmagick
-   [Gmagick::shearimage](gmagick.shearimage.md) - Створює паралелограм
-   [Gmagick::solarizeimage](gmagick.solarizeimage.md) — Застосовує ефект соляризації до зображення.
-   [Gmagick::spreadimage](gmagick.spreadimage.md) — Випадково зміщує кожен піксель у блоці
-   [Gmagick::stripimage](gmagick.stripimage.md) — Знімає зображення всіх профілів та коментарів
-   [Gmagick::swirlimage](gmagick.swirlimage.md) — Закручує пікселі навколо центру зображення
-   [Gmagick::thumbnailimage](gmagick.thumbnailimage.md) — Змінює розмір зображення
-   [Gmagick::trimimage](gmagick.trimimage.md) — Видаляє краї зображення
-   [Gmagick::write](gmagick.write.md) - Псевдонім Gmagick:: writeimage
-   [Gmagick::writeimage](gmagick.writeimage.md) — Записує зображення у вказаний файл