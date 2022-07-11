- [« Imagick::solarizeImage](imagick.solarizeimage.md)
- [Imagick::spliceImage »](imagick.spliceimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Інтерполює кольори

# Imagick::sparseColorImage

(PECL imagick 2 \>= 2.3.0, PECL imagick 3)

Imagick::sparseColorImage — Інтерполує кольори

### Опис

public **Imagick::sparseColorImage**(int `$SPARSE_METHOD`, array
`$arguments`, int `$channel` = Imagick::CHANNEL_DEFAULT): bool

Враховуючи масив аргументів, що містить числові значення, метод
інтерполує кольори, знайдені з цими координатами, по всьому
зображенню, використовуючи `sparse_method`. Цей метод доступний, якщо
Imagick був скомпілюваний з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`SPARSE_METHOD`
Зверніться до списку [sparse method constants](imagick.constants.md#imagick.constants.sparsecolormethod)

`arguments`
Масив, що містить координати. Масив у форматі `array(1,1, 2,45)`

`channel`
Надайте будь-яку коректну для вашого режиму каналу константу. Для
застосування до більш ніж одного каналу, комбінуйте [константи каналов](imagick.constants.md#imagick.constants.channel) за допомогою
побітових операторів. За промовчанням одно **`Imagick::CHANNEL_DEFAULT`**.
Зверніться до списку [констант каналов](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 SPARSECOLORMETHOD_BARYCENTRIC
**Imagick::sparseColorImage()****

` <?php    function renderImageBarycentric2() {        $points = [            [0.30, 0.10, 'red'],            [0.10, 0.80, 'blue'],            [0.70, 0.60, 'lime'],            [0.80, 0.20, 'yellow '],        ]; $imagick = createGradientImage(          | header("Content-Type: image/png"); echo $imagick->getImageBlob(); }?> `

**Приклад #2 SPARSECOLORMETHOD_BILINEAR **Imagick::sparseColorImage()****

`<?php                                                 0 '],]; $imagick = createGradientImage(500, 500, $points, \Imagick::SPARSECOLORMETHOD_BILINEAR); header("Content-Type: image/png"); echo $imagick->getImageBlob(); }?> `

**Приклад #3 SPARSECOLORMETHOD_SPEPARDS **Imagick::sparseColorImage()****

` <?php    function renderImageShepards() {        $points = [            [0.30, 0.10, 'red'],            [0.10, 0.80, 'blue'],            [0.70, 0.60, 'lime'],            [0.80, 0.20, 'yellow '],        ]; $imagick = createGradientImage(600, 600, $points, \Imagick::SPARSECOLORMETHOD_SPEPARDS); header("Content-Type: image/png"); echo $imagick->getImageBlob(); }?> `

**Приклад #4 SPARSECOLORMETHOD_VORONOI **Imagick::sparseColorImage()****

` <?php    function renderImageVoronoi() {        $points = [            [0.30, 0.10, 'red'],            [0.10, 0.80, 'blue'],            [0.70, 0.60, 'lime'],            [0.80, 0.20, 'yellow '],        ]; $imagick = createGradientImage(500, 500, $points, \Imagick::SPARSECOLORMETHOD_VORONOI); header("Content-Type: image/png"); echo $imagick->getImageBlob(); }?> `

**Приклад #5 SPARSECOLORMETHOD_BARYCENTRIC
**Imagick::sparseColorImage()****

` <?php    function renderImageBarycentric() {        $points = [            [0, 0, 'skyblue'],            [-1, 1, 'skyblue'],            [1, 1, 'black'],        ]; $imagick = createGradientImage(600, 200, $points, \Imagick::SPARSECOLORMETHOD_BARYCENTRIC); header("Content-Type: image/png"); echo $imagick->getImageBlob(); }?> `

**Приклад #6 createGradientImage is used by other examples.
**Imagick::sparseColorImage()****

` <?phpfunction createGradientImage($width, $height, $colorPoints, $sparseMethod, $absolute = false) {    $imagick = new \Imagick(); $imagick->newImage($width, $height, "white"); $imagick->setImageFormat("png"); $barycentricPoints==array(); foreach ($colorPoints as $colorPoint) {        if ($absolute == true) {            $barycentricPoints[] | $barycentricPoints[] = $colorPoint[1]; }||||||||||| $barycentricPoints[] = $colorPoint[1] * $height; }       if (is_string($colorPoint[2])) {           $imagickPixel==new \ImagickPixel($colorPoint[2]); }    else if ($colorPoint[2] instanceof \ImagickPixel) {            $imagickPixel = $colorPoint[2]; }        else{            $errorMessage = sprintf(                "Значение %s не является ни строкой, ни классом ImagickPixel. Не может использовать в качестве цвета.",                $colorPoint[2]            ); throw new \InvalidArgumentException(                $errorMessage              ); }        $red = $imagickPixel->getColorValue(\Imagick::COLOR_RED); $green= $imagickPixel->getColorValue(\Imagick::COLOR_GREEN); $blue = $imagickPixel->getColorValue(\Imagick::COLOR_BLUE); $alpha==$imagickPixel->getColorValue(\Imagick::COLOR_ALPHA); $barycentricPoints[] = $red; $barycentricPoints[] = $green; $barycentricPoints[] = $blue; $barycentricPoints[] = $alpha; }   $imagick->sparseColorImage($sparseMethod,$barycentricPoints); return $imagick;}?> `
