Клас Gmagick

-   [« Примеры](gmagick.examples.html)
    
-   [Gmagick::addimage »](gmagick.addimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](book.gmagick.html)
    
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

-   [Gmagick::addimage](gmagick.addimage.html) — Додавання нового зображення до списку зображень об'єкта Gmagick
-   [Gmagick::addnoiseimage](gmagick.addnoiseimage.html) — Додає випадкового шуму до зображення
-   [Gmagick::annotateimage](gmagick.annotateimage.html) — Підписати зображення текстом
-   [Gmagick::blurimage](gmagick.blurimage.html) — Додати розмиття зображення
-   [Gmagick::borderimage](gmagick.borderimage.html) — Додати рамку до зображення
-   [Gmagick::charcoalimage](gmagick.charcoalimage.html) — Імітація малювання вугіллям
-   [Gmagick::chopimage](gmagick.chopimage.html) — Видаляє область зображення та підрізає його.
-   [Gmagick::clear](gmagick.clear.html) — Зачищає всі ресурси, пов'язані з об'єктом Gmagick
-   [Gmagick::commentimage](gmagick.commentimage.html) — Додати коментар до зображення
-   [Gmagick::compositeimage](gmagick.compositeimage.html) — Накладає одне зображення на інше
-   [Gmagick::\_\_construct](gmagick.construct.html) - Конструктор об'єкта Gmagick
-   [Gmagick::cropimage](gmagick.cropimage.html) — Обрізає зображення
-   [Gmagick::cropthumbnailimage](gmagick.cropthumbnailimage.html) — Створення обрізаного зменшеного зображення
-   [Gmagick::current](gmagick.current.html) - Повернути самого себе
-   [Gmagick::cyclecolormapimage](gmagick.cyclecolormapimage.html) — Зміщує колірну карту зображення
-   [Gmagick::deconstructimages](gmagick.deconstructimages.html) — Повертає певні піксельні відмінності між зображеннями
-   [Gmagick::despeckleimage](gmagick.despeckleimage.html) - Призначення despeckleimage
-   [Gmagick::destroy](gmagick.destroy.html) — Знищити об'єкт Gmagick
-   [Gmagick::drawimage](gmagick.drawimage.html) — Відображає об'єкт GmagickDraw на поточному зображенні
-   [Gmagick::edgeimage](gmagick.edgeimage.html) — Збільшує краї зображення.
-   [Gmagick::embossimage](gmagick.embossimage.html) — Повертає зображення у градаціях сірого із тривимірним ефектом
-   [Gmagick::enhanceimage](gmagick.enhanceimage.html) — Покращує якість зображення із шумом
-   [Gmagick::equalizeimage](gmagick.equalizeimage.html) — Вирівнює гістограму зображення
-   [Gmagick::flipimage](gmagick.flipimage.html) — Створює вертикальне дзеркальне відображення
-   [Gmagick::flopimage](gmagick.flopimage.html) — Створює горизонтальне дзеркальне відображення
-   [Gmagick::frameimage](gmagick.frameimage.html) — Додає змодельований тривимірний кордон
-   [Gmagick::gammaimage](gmagick.gammaimage.html) - Гамма-корекція зображення
-   [Gmagick::getcopyright](gmagick.getcopyright.html) — Повертає копірайт GraphicsMagick API у вигляді рядка
-   [Gmagick::getfilename](gmagick.getfilename.html) — Повертає ім'я файлу, пов'язаного з послідовністю зображень.
-   [Gmagick::getimagebackgroundcolor](gmagick.getimagebackgroundcolor.html) — Повертає колір тла зображення
-   [Gmagick::getimageblueprimary](gmagick.getimageblueprimary.html) — Повертає кольоровість синьої первинної точки
-   [Gmagick::getimagebordercolor](gmagick.getimagebordercolor.html) — Повертає колір кордону зображення
-   [Gmagick::getimagechanneldepth](gmagick.getimagechanneldepth.html) — Отримує глибину для певного каналу зображення
-   [Gmagick::getimagecolors](gmagick.getimagecolors.html) — Повертає колір зазначеного індексу карти кольорів
-   [Gmagick::getimagecolorspace](gmagick.getimagecolorspace.html) — Повертає колірний простір зображення
-   [Gmagick::getimagecompose](gmagick.getimagecompose.html) — Повертає складовий оператор, пов'язаний із зображенням
-   [Gmagick::getimagedelay](gmagick.getimagedelay.html) — Отримує затримку зображення
-   [Gmagick::getimagedepth](gmagick.getimagedepth.html) — Отримує глибину зображення
-   [Gmagick::getimagedispose](gmagick.getimagedispose.html) — Отримує метод видалення зображення
-   [Gmagick::getimageextrema](gmagick.getimageextrema.html) — Отримує екстремуми для зображення
-   [Gmagick::getimagefilename](gmagick.getimagefilename.html) — Повертає ім'я файлу конкретного зображення у послідовності
-   [Gmagick::getimageformat](gmagick.getimageformat.html) — Повертає формат зображення в послідовності.
-   [Gmagick::getimagegamma](gmagick.getimagegamma.html) — Повертає гаму зображення
-   [Gmagick::getimagegreenprimary](gmagick.getimagegreenprimary.html) — Повертає первинну зелену точку
-   [Gmagick::getimageheight](gmagick.getimageheight.html) — Повертає висоту зображення
-   [Gmagick::getimagehistogram](gmagick.getimagehistogram.html) — Повертає гістограму зображення
-   [Gmagick::getimageindex](gmagick.getimageindex.html) — Повертає індекс активного поточного зображення.
-   [Gmagick::getimageinterlacescheme](gmagick.getimageinterlacescheme.html) — Отримує схему чергування зображень
-   [Gmagick::getimageiterations](gmagick.getimageiterations.html) — Отримує ітерацію зображення
-   [Gmagick::getimagematte](gmagick.getimagematte.html) — Перевіряє, чи є на зображенні матовий канал
-   [Gmagick::getimagemattecolor](gmagick.getimagemattecolor.html) — Повертає зображення матового кольору
-   [Gmagick::getimageprofile](gmagick.getimageprofile.html) — Повертає іменований профайл зображення
-   [Gmagick::getimageredprimary](gmagick.getimageredprimary.html) — Повертає первинну червону точку
-   [Gmagick::getimagerenderingintent](gmagick.getimagerenderingintent.html) — Отримує мету рендерингу зображення
-   [Gmagick::getimageresolution](gmagick.getimageresolution.html) — Повертає роздільну здатність зображення
-   [Gmagick::getimagescene](gmagick.getimagescene.html) — Отримує сцену зображення
-   [Gmagick::getimagesignature](gmagick.getimagesignature.html) — Створює підпис до повідомлення SHA-256
-   [Gmagick::getimagetype](gmagick.getimagetype.html) — Повертає потенційний тип зображення
-   [Gmagick::getimageunits](gmagick.getimageunits.html) — Повертає одиниці роздільної здатності зображення
-   [Gmagick::getimagewhitepoint](gmagick.getimagewhitepoint.html) — Повертає хроматичну білу крапку
-   [Gmagick::getimagewidth](gmagick.getimagewidth.html) — Повертає ширину зображення
-   [Gmagick::getpackagename](gmagick.getpackagename.html) — Повертає ім'я пакета GraphicsMagick
-   [Gmagick::getquantumdepth](gmagick.getquantumdepth.html) — Повертає глибину кольору (біт на канал) об'єкта Gmagick у вигляді рядка
-   [Gmagick::getreleasedate](gmagick.getreleasedate.html) — Повертає дату релізу GraphicsMagick у вигляді рядка
-   [Gmagick::getsamplingfactors](gmagick.getsamplingfactors.html) — Повертає вертикальний та горизонтальний фактор дискретизації
-   [Gmagick::getsize](gmagick.getsize.html) — Повертає розмір, пов'язаний із об'єктом Gmagick
-   [Gmagick::getversion](gmagick.getversion.html) — Повертає версію GraphicsMagick API
-   [Gmagick::hasnextimage](gmagick.hasnextimage.html) — Перевіряє, чи є ще зображення в об'єкті
-   [Gmagick::haspreviousimage](gmagick.haspreviousimage.html) — Перевіряє, чи є ще зображення в об'єкті під час ітерації назад
-   [Gmagick::implodeimage](gmagick.implodeimage.html) — Створює копію зображення
-   [Gmagick::labelimage](gmagick.labelimage.html) — Додає позначку до зображення
-   [Gmagick::levelimage](gmagick.levelimage.html) — Регулює рівні зображення
-   [Gmagick::magnifyimage](gmagick.magnifyimage.html) - Пропорційно масштабує зображення в 2 рази
-   [Gmagick::mapimage](gmagick.mapimage.html) — Замінює кольори зображення на найближчий колір із еталонного зображення
-   [Gmagick::medianfilterimage](gmagick.medianfilterimage.html) — Застосовує цифровий фільтр
-   [Gmagick::minifyimage](gmagick.minifyimage.html) — Масштабує зображення пропорційно до половини його розміру.
-   [Gmagick::modulateimage](gmagick.modulateimage.html) — Керує яскравістю, насиченістю та відтінком
-   [Gmagick::motionblurimage](gmagick.motionblurimage.html) — Імітує розмиття під час руху
-   [Gmagick::newimage](gmagick.newimage.html) — Створює нове зображення
-   [Gmagick::nextimage](gmagick.nextimage.html) — Здійснює перехід до наступного зображення
-   [Gmagick::normalizeimage](gmagick.normalizeimage.html) — Підвищує контрастність кольорового зображення
-   [Gmagick::oilpaintimage](gmagick.oilpaintimage.html) — Імітує ефект картини олією
-   [Gmagick::previousimage](gmagick.previousimage.html) — Здійснює перехід до попереднього зображення в об'єкті
-   [Gmagick::profileimage](gmagick.profileimage.html) — Додає або видаляє профіль із зображення.
-   [Gmagick::quantizeimage](gmagick.quantizeimage.html) - Аналізує кольори еталонного зображення
-   [Gmagick::quantizeimages](gmagick.quantizeimages.html) — Аналізує кольори у послідовності зображень
-   [Gmagick::queryfontmetrics](gmagick.queryfontmetrics.html) — Повертає масив, який представляє метрики шрифту
-   [Gmagick::queryfonts](gmagick.queryfonts.html) — Повертає налаштовані шрифти
-   [Gmagick::queryformats](gmagick.queryformats.html) — Повертає формати Gmagick.
-   [Gmagick::radialblurimage](gmagick.radialblurimage.html) — Застосовує радіальне розмиття зображення.
-   [Gmagick::raiseimage](gmagick.raiseimage.html) — Створює імітацію ефекту тривимірної кнопки
-   [Gmagick::read](gmagick.read.html) — Читає зображення із файлу
-   [Gmagick::readimage](gmagick.readimage.html) — Читає зображення із файлу
-   [Gmagick::readimageblob](gmagick.readimageblob.html) — Читає зображення з бінарного рядка
-   [Gmagick::readimagefile](gmagick.readimagefile.html) — Читає зображення або послідовність зображень із файлового дескриптора
-   [Gmagick::reducenoiseimage](gmagick.reducenoiseimage.html) — Згладжує контури зображення
-   [Gmagick::removeimage](gmagick.removeimage.html) — Видаляє зображення зі списку
-   [Gmagick::removeimageprofile](gmagick.removeimageprofile.html) — Видаляє іменований профайл зображення та повертає його
-   [Gmagick::resampleimage](gmagick.resampleimage.html) — Змінює роздільну здатність зображення до бажаного.
-   [Gmagick::resizeimage](gmagick.resizeimage.html) — Масштабує зображення
-   [Gmagick::rollimage](gmagick.rollimage.html) — Зміщує зображення
-   [Gmagick::rotateimage](gmagick.rotateimage.html) — Повертає зображення
-   [Gmagick::scaleimage](gmagick.scaleimage.html) — Масштабує розмір зображення
-   [Gmagick::separateimagechannel](gmagick.separateimagechannel.html) — Відокремлює канал від зображення.
-   [Gmagick::setCompressionQuality](gmagick.setcompressionquality.html) — Встановлює якість стандартного стиснення об'єкта
-   [Gmagick::setfilename](gmagick.setfilename.html) — Встановлює ім'я файлу перед читанням чи записом зображення
-   [Gmagick::setimagebackgroundcolor](gmagick.setimagebackgroundcolor.html) — Встановлює колір тла зображення
-   [Gmagick::setimageblueprimary](gmagick.setimageblueprimary.html) — Встановлює кольоровість зображення блакитною основною точкою.
-   [Gmagick::setimagebordercolor](gmagick.setimagebordercolor.html) — Встановлює колір рамки зображення
-   [Gmagick::setimagechanneldepth](gmagick.setimagechanneldepth.html) — Встановлює глибину певного каналу зображення
-   [Gmagick::setimagecolorspace](gmagick.setimagecolorspace.html) — Встановлює колірний простір зображення
-   [Gmagick::setimagecompose](gmagick.setimagecompose.html) — Встановлює оператор складеного зображення
-   [Gmagick::setimagedelay](gmagick.setimagedelay.html) — Встановлює затримку зображення
-   [Gmagick::setimagedepth](gmagick.setimagedepth.html) — Встановлює глибину зображення
-   [Gmagick::setimagedispose](gmagick.setimagedispose.html) — Встановлює метод видалення зображення
-   [Gmagick::setimagefilename](gmagick.setimagefilename.html) — Встановлює ім'я файлу конкретного зображення у послідовності
-   [Gmagick::setimageformat](gmagick.setimageformat.html) — Встановлює формат певного зображення
-   [Gmagick::setimagegamma](gmagick.setimagegamma.html) — Встановлює гаму зображення
-   [Gmagick::setimagegreenprimary](gmagick.setimagegreenprimary.html) — Встановлює кольоровість зображення зеленою первинною точкою.
-   [Gmagick::setimageindex](gmagick.setimageindex.html) — Встановлює ітератор у положення списку зображень, заданому параметром index
-   [Gmagick::setimageinterlacescheme](gmagick.setimageinterlacescheme.html) — Встановлює схему надстрокової розгортки зображення
-   [Gmagick::setimageiterations](gmagick.setimageiterations.html) — Встановлює ітерацію зображення
-   [Gmagick::setimageprofile](gmagick.setimageprofile.html) — Додає іменований профіль до об'єкту Gmagick
-   [Gmagick::setimageredprimary](gmagick.setimageredprimary.html) — Встановлює кольоровість зображення червоною основною точкою.
-   [Gmagick::setimagerenderingintent](gmagick.setimagerenderingintent.html) — Встановлює спосіб рендерингу зображення
-   [Gmagick::setimageresolution](gmagick.setimageresolution.html) — Встановлює роздільну здатність зображення
-   [Gmagick::setimagescene](gmagick.setimagescene.html) — Встановлює сцену зображення
-   [Gmagick::setimagetype](gmagick.setimagetype.html) — Встановлює тип зображення
-   [Gmagick::setimageunits](gmagick.setimageunits.html) — Встановлює одиниці роздільної здатності зображення
-   [Gmagick::setimagewhitepoint](gmagick.setimagewhitepoint.html) — Встановлює кольоровість зображення білою точкою.
-   [Gmagick::setsamplingfactors](gmagick.setsamplingfactors.html) — Встановлює фактори вибірки зображення
-   [Gmagick::setsize](gmagick.setsize.html) — Встановлює розмір об'єкта Gmagick
-   [Gmagick::shearimage](gmagick.shearimage.html) - Створює паралелограм
-   [Gmagick::solarizeimage](gmagick.solarizeimage.html) — Застосовує ефект соляризації до зображення.
-   [Gmagick::spreadimage](gmagick.spreadimage.html) — Випадково зміщує кожен піксель у блоці
-   [Gmagick::stripimage](gmagick.stripimage.html) — Знімає зображення всіх профілів та коментарів
-   [Gmagick::swirlimage](gmagick.swirlimage.html) — Закручує пікселі навколо центру зображення
-   [Gmagick::thumbnailimage](gmagick.thumbnailimage.html) — Змінює розмір зображення
-   [Gmagick::trimimage](gmagick.trimimage.html) — Видаляє краї зображення
-   [Gmagick::write](gmagick.write.html) - Псевдонім Gmagick:: writeimage
-   [Gmagick::writeimage](gmagick.writeimage.html) — Записує зображення у вказаний файл