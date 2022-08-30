Клас Imagick

-   [« Базовое использование](imagick.examples-1.html)
    
-   [Imagick::adaptiveBlurImage »](imagick.adaptiveblurimage.html)
    
-   [PHP Manual](index.html)
    
-   [ImageMagick](book.imagick.html)
    
-   Клас Imagick
    

# Клас [Imagick](class.imagick.html)

(PECL imagick 2, PECL imagick 3)

## Огляд класів

```classsynopsis

    
     class Imagick
     implements 
       Iterator {
    
   public __construct(mixed $files = ?)

    public adaptiveBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
public adaptiveResizeImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
public adaptiveSharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
public adaptiveThresholdImage(int $width, int $height, int $offset): bool
public addImage(Imagick $source): bool
public addNoiseImage(int $noise_type, int $channel = Imagick::CHANNEL_DEFAULT): bool
public affineTransformImage(ImagickDraw $matrix): bool
public animateImages(string $x_server): bool
public annotateImage(    ImagickDraw $draw_settings,    float $x,    float $y,    float $angle,    string $text): bool
public appendImages(bool $stack): Imagick
public autoLevelImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
public averageImages(): Imagick
public blackThresholdImage(mixed $threshold): bool
public blueShiftImage(float $factor = 1.5): bool
public blurImage(float $radius, float $sigma, int $channel = ?): bool
public borderImage(mixed $bordercolor, int $width, int $height): bool
public brightnessContrastImage(float $brightness, float $contrast, int $channel = Imagick::CHANNEL_DEFAULT): bool
public charcoalImage(float $radius, float $sigma): bool
public chopImage(    int $width,    int $height,    int $x,    int $y): bool
public clampImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
public clear(): bool
public clipImage(): bool
public clipImagePath(string $pathname, string $inside): void
public clipPathImage(string $pathname, bool $inside): bool
public clone(): Imagick
public clutImage(Imagick $lookup_table, int $channel = Imagick::CHANNEL_DEFAULT): bool
public coalesceImages(): Imagick
public colorFloodfillImage(    mixed $fill,    float $fuzz,    mixed $bordercolor,    int $x,    int $y): bool
public colorizeImage(mixed $colorize, mixed $opacity, bool $legacy = false): bool
public colorMatrixImage(array $color_matrix = Imagick::CHANNEL_DEFAULT): bool
public combineImages(int $channelType): Imagick
public commentImage(string $comment): bool
public compareImageChannels(Imagick $image, int $channelType, int $metricType): array
public compareImageLayers(int $method): Imagick
public compareImages(Imagick $compare, int $metric): array
public compositeImage(    Imagick $composite_object,    int $composite,    int $x,    int $y,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public contrastImage(bool $sharpen): bool
public contrastStretchImage(float $black_point, float $white_point, int $channel = Imagick::CHANNEL_DEFAULT): bool
public convolveImage(array $kernel, int $channel = Imagick::CHANNEL_DEFAULT): bool
public count(int $mode = 0): int
public cropImage(    int $width,    int $height,    int $x,    int $y): bool
public cropThumbnailImage(int $width, int $height, bool $legacy = false): bool
public current(): Imagick
public cycleColormapImage(int $displace): bool
public decipherImage(string $passphrase): bool
public deconstructImages(): Imagick
public deleteImageArtifact(string $artifact): bool
public deleteImageProperty(string $name): bool
public deskewImage(float $threshold): bool
public despeckleImage(): bool
public destroy(): bool
public displayImage(string $servername): bool
public displayImages(string $servername): bool
public distortImage(int $method, array $arguments, bool $bestfit): bool
public drawImage(ImagickDraw $draw): bool
public edgeImage(float $radius): bool
public embossImage(float $radius, float $sigma): bool
public encipherImage(string $passphrase): bool
public enhanceImage(): bool
public equalizeImage(): bool
public evaluateImage(int $op, float $constant, int $channel = Imagick::CHANNEL_DEFAULT): bool
public exportImagePixels(    int $x,    int $y,    int $width,    int $height,    string $map,    int $STORAGE): array
public extentImage(    int $width,    int $height,    int $x,    int $y): bool
public filter(ImagickKernel $ImagickKernel, int $channel = Imagick::CHANNEL_UNDEFINED): bool
public flattenImages(): Imagick
public flipImage(): bool
public floodFillPaintImage(    mixed $fill,    float $fuzz,    mixed $target,    int $x,    int $y,    bool $invert,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public flopImage(): bool
public forwardFourierTransformimage(bool $magnitude): bool
public frameImage(    mixed $matte_color,    int $width,    int $height,    int $inner_bevel,    int $outer_bevel): bool
public functionImage(int $function, array $arguments, int $channel = Imagick::CHANNEL_DEFAULT): bool
public fxImage(string $expression, int $channel = Imagick::CHANNEL_DEFAULT): Imagick
public gammaImage(float $gamma, int $channel = Imagick::CHANNEL_DEFAULT): bool
public gaussianBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
public getColorspace(): int
public getCompression(): int
public getCompressionQuality(): int
public static getCopyright(): string
public getFilename(): string
public getFont(): string
public getFormat(): string
public getGravity(): int
public static getHomeURL(): string
public getImage(): Imagick
public getImageAlphaChannel(): bool
public getImageArtifact(string $artifact): string
public getImageAttribute(string $key): string
public getImageBackgroundColor(): ImagickPixel
public getImageBlob(): string
public getImageBluePrimary(): array
public getImageBorderColor(): ImagickPixel
public getImageChannelDepth(int $channel): int
public getImageChannelDistortion(Imagick $reference, int $channel, int $metric): float
public getImageChannelDistortions(Imagick $reference, int $metric, int $channel = Imagick::CHANNEL_DEFAULT): float
public getImageChannelExtrema(int $channel): array
public getImageChannelKurtosis(int $channel = Imagick::CHANNEL_DEFAULT): array
public getImageChannelMean(int $channel): array
public getImageChannelRange(int $channel): array
public getImageChannelStatistics(): array
public getImageClipMask(): Imagick
public getImageColormapColor(int $index): ImagickPixel
public getImageColors(): int
public getImageColorspace(): int
public getImageCompose(): int
public getImageCompression(): int
public getImageCompressionQuality(): int
public getImageDelay(): int
public getImageDepth(): int
public getImageDispose(): int
public getImageDistortion(MagickWand $reference, int $metric): float
public getImageExtrema(): array
public getImageFilename(): string
public getImageFormat(): string
public getImageGamma(): float
public getImageGeometry(): array
public getImageGravity(): int
public getImageGreenPrimary(): array
public getImageHeight(): int
public getImageHistogram(): array
public getImageIndex(): int
public getImageInterlaceScheme(): int
public getImageInterpolateMethod(): int
public getImageIterations(): int
public getImageLength(): int
public getImageMatte(): bool
public getImageMatteColor(): ImagickPixel
public getImageMimeType(): string
public getImageOrientation(): int
public getImagePage(): array
public getImagePixelColor(int $x, int $y): ImagickPixel
public getImageProfile(string $name): string
public getImageProfiles(string $pattern = "*", bool $include_values = true): array
public getImageProperties(string $pattern = "*", bool $include_values = true): array
public getImageProperty(string $name): string
public getImageRedPrimary(): array
public getImageRegion(    int $width,    int $height,    int $x,    int $y): Imagick
public getImageRenderingIntent(): int
public getImageResolution(): array
public getImagesBlob(): string
public getImageScene(): int
public getImageSignature(): string
public getImageSize(): int
public getImageTicksPerSecond(): int
public getImageTotalInkDensity(): float
public getImageType(): int
public getImageUnits(): int
public getImageVirtualPixelMethod(): int
public getImageWhitePoint(): array
public getImageWidth(): int
public getInterlaceScheme(): int
public getIteratorIndex(): int
public getNumberImages(): int
public getOption(string $key): string
public static getPackageName(): string
public getPage(): array
public getPixelIterator(): ImagickPixelIterator
public getPixelRegionIterator(    int $x,    int $y,    int $columns,    int $rows): ImagickPixelIterator
public getPointSize(): float
public static getQuantum(): int
public static getQuantumDepth(): array
public static getQuantumRange(): array
public static getRegistry(string $key): string
public static getReleaseDate(): string
public static getResource(int $type): int
public static getResourceLimit(int $type): int
public getSamplingFactors(): array
public getSize(): array
public getSizeOffset(): int
public static getVersion(): array
public haldClutImage(Imagick $clut, int $channel = Imagick::CHANNEL_DEFAULT): bool
public hasNextImage(): bool
public hasPreviousImage(): bool
public identifyFormat(string $embedText): string|false
public identifyImage(bool $appendRawOutput = false): array
public implodeImage(float $radius): bool
public importImagePixels(    int $x,    int $y,    int $width,    int $height,    string $map,    int $storage,    array $pixels): bool
public inverseFourierTransformImage(Imagick $complement, bool $magnitude): bool
public labelImage(string $label): bool
public levelImage(    float $blackPoint,    float $gamma,    float $whitePoint,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public linearStretchImage(float $blackPoint, float $whitePoint): bool
public liquidRescaleImage(    int $width,    int $height,    float $delta_x,    float $rigidity): bool
public static listRegistry(): array
public magnifyImage(): bool
public mapImage(Imagick $map, bool $dither): bool
public matteFloodfillImage(    float $alpha,    float $fuzz,    mixed $bordercolor,    int $x,    int $y): bool
public medianFilterImage(float $radius): bool
public mergeImageLayers(int $layer_method): Imagick
public minifyImage(): bool
public modulateImage(float $brightness, float $saturation, float $hue): bool
public montageImage(    ImagickDraw $draw,    string $tile_geometry,    string $thumbnail_geometry,    int $mode,    string $frame): Imagick
public morphImages(int $number_frames): Imagick
public morphology(    int $morphologyMethod,    int $iterations,    ImagickKernel $ImagickKernel,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public mosaicImages(): Imagick
public motionBlurImage(    float $radius,    float $sigma,    float $angle,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public negateImage(bool $gray, int $channel = Imagick::CHANNEL_DEFAULT): bool
public newImage(    int $cols,    int $rows,    mixed $background,    string $format = ?): bool
public newPseudoImage(int $columns, int $rows, string $pseudoString): bool
public nextImage(): bool
public normalizeImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
public oilPaintImage(float $radius): bool
public opaquePaintImage(    mixed $target,    mixed $fill,    float $fuzz,    bool $invert,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public optimizeImageLayers(): bool
public orderedPosterizeImage(string $threshold_map, int $channel = Imagick::CHANNEL_DEFAULT): bool
public paintFloodfillImage(    mixed $fill,    float $fuzz,    mixed $bordercolor,    int $x,    int $y,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public paintOpaqueImage(    mixed $target,    mixed $fill,    float $fuzz,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public paintTransparentImage(mixed $target, float $alpha, float $fuzz): bool
public pingImage(string $filename): bool
public pingImageBlob(string $image): bool
public pingImageFile(resource $filehandle, string $fileName = ?): bool
public polaroidImage(ImagickDraw $properties, float $angle): bool
public posterizeImage(int $levels, bool $dither): bool
public previewImages(int $preview): bool
public previousImage(): bool
public profileImage(string $name, string $profile): bool
public quantizeImage(    int $numberColors,    int $colorspace,    int $treedepth,    bool $dither,    bool $measureError): bool
public quantizeImages(    int $numberColors,    int $colorspace,    int $treedepth,    bool $dither,    bool $measureError): bool
public queryFontMetrics(ImagickDraw $properties, string $text, bool $multiline = ?): array
public static queryFonts(string $pattern = "*"): array
public static queryFormats(string $pattern = "*"): array
public radialBlurImage(float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
public raiseImage(    int $width,    int $height,    int $x,    int $y,    bool $raise): bool
public randomThresholdImage(float $low, float $high, int $channel = Imagick::CHANNEL_DEFAULT): bool
public readImage(string $filename): bool
public readImageBlob(string $image, string $filename = ?): bool
public readImageFile(resource $filehandle, string $fileName = null): bool
public readImages(array $filenames): bool
public recolorImage(array $matrix): bool
public reduceNoiseImage(float $radius): bool
public remapImage(Imagick $replacement, int $DITHER): bool
public removeImage(): bool
public removeImageProfile(string $name): string
public render(): bool
public resampleImage(    float $x_resolution,    float $y_resolution,    int $filter,    float $blur): bool
public resetImagePage(string $page): bool
public resizeImage(    int $columns,    int $rows,    int $filter,    float $blur,    bool $bestfit = false,    bool $legacy = false): bool
public rollImage(int $x, int $y): bool
public rotateImage(mixed $background, float $degrees): bool
public rotationalBlurImage(float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
public roundCorners(    float $x_rounding,    float $y_rounding,    float $stroke_width = 10,    float $displace = 5,    float $size_correction = -6): bool
public sampleImage(int $columns, int $rows): bool
public scaleImage(    int $cols,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
public segmentImage(    int $COLORSPACE,    float $cluster_threshold,    float $smooth_threshold,    bool $verbose = false): bool
public selectiveBlurImage(    float $radius,    float $sigma,    float $threshold,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public separateImageChannel(int $channel): bool
public sepiaToneImage(float $threshold): bool
public setBackgroundColor(mixed $background): bool
public setColorspace(int $COLORSPACE): bool
public setCompression(int $compression): bool
public setCompressionQuality(int $quality): bool
public setFilename(string $filename): bool
public setFirstIterator(): bool
public setFont(string $font): bool
public setFormat(string $format): bool
public setGravity(int $gravity): bool
public setImage(Imagick $replace): bool
public setImageAlphaChannel(int $mode): bool
public setImageArtifact(string $artifact, string $value): bool
public setImageAttribute(string $key, string $value): bool
public setImageBackgroundColor(mixed $background): bool
public setImageBias(float $bias): bool
public setImageBiasQuantum(string $bias): void
public setImageBluePrimary(float $x, float $y): bool
public setImageBorderColor(mixed $border): bool
public setImageChannelDepth(int $channel, int $depth): bool
public setImageClipMask(Imagick $clip_mask): bool
public setImageColormapColor(int $index, ImagickPixel $color): bool
public setImageColorspace(int $colorspace): bool
public setImageCompose(int $compose): bool
public setImageCompression(int $compression): bool
public setImageCompressionQuality(int $quality): bool
public setImageDelay(int $delay): bool
public setImageDepth(int $depth): bool
public setImageDispose(int $dispose): bool
public setImageExtent(int $columns, int $rows): bool
public setImageFilename(string $filename): bool
public setImageFormat(string $format): bool
public setImageGamma(float $gamma): bool
public setImageGravity(int $gravity): bool
public setImageGreenPrimary(float $x, float $y): bool
public setImageIndex(int $index): bool
public setImageInterlaceScheme(int $interlace_scheme): bool
public setImageInterpolateMethod(int $method): bool
public setImageIterations(int $iterations): bool
public setImageMatte(bool $matte): bool
public setImageMatteColor(mixed $matte): bool
public setImageOpacity(float $opacity): bool
public setImageOrientation(int $orientation): bool
public setImagePage(    int $width,    int $height,    int $x,    int $y): bool
public setImageProfile(string $name, string $profile): bool
public setImageProperty(string $name, string $value): bool
public setImageRedPrimary(float $x, float $y): bool
public setImageRenderingIntent(int $rendering_intent): bool
public setImageResolution(float $x_resolution, float $y_resolution): bool
public setImageScene(int $scene): bool
public setImageTicksPerSecond(int $ticks_per_second): bool
public setImageType(int $image_type): bool
public setImageUnits(int $units): bool
public setImageVirtualPixelMethod(int $method): bool
public setImageWhitePoint(float $x, float $y): bool
public setInterlaceScheme(int $interlace_scheme): bool
public setIteratorIndex(int $index): bool
public setLastIterator(): bool
public setOption(string $key, string $value): bool
public setPage(    int $width,    int $height,    int $x,    int $y): bool
public setPointSize(float $point_size): bool
public setProgressMonitor(callable $callback): bool
public static setRegistry(string $key, string $value): bool
public setResolution(float $x_resolution, float $y_resolution): bool
public static setResourceLimit(int $type, int $limit): bool
public setSamplingFactors(array $factors): bool
public setSize(int $columns, int $rows): bool
public setSizeOffset(int $columns, int $rows, int $offset): bool
public setType(int $image_type): bool
public shadeImage(bool $gray, float $azimuth, float $elevation): bool
public shadowImage(    float $opacity,    float $sigma,    int $x,    int $y): bool
public sharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
public shaveImage(int $columns, int $rows): bool
public shearImage(mixed $background, float $x_shear, float $y_shear): bool
public sigmoidalContrastImage(    bool $sharpen,    float $alpha,    float $beta,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public sketchImage(float $radius, float $sigma, float $angle): bool
public smushImages(bool $stack, int $offset): Imagick
public solarizeImage(int $threshold): bool
public sparseColorImage(int $SPARSE_METHOD, array $arguments, int $channel = Imagick::CHANNEL_DEFAULT): bool
public spliceImage(    int $width,    int $height,    int $x,    int $y): bool
public spreadImage(float $radius): bool
public statisticImage(    int $type,    int $width,    int $height,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public steganoImage(Imagick $watermark_wand, int $offset): Imagick
public stereoImage(Imagick $offset_wand): bool
public stripImage(): bool
public subImageMatch(Imagick $Imagick, array &$offset = ?, float &$similarity = ?): Imagick
swirlImage(float $degrees): bool
textureImage(Imagick $texture_wand): Imagick
public thresholdImage(float $threshold, int $channel = Imagick::CHANNEL_DEFAULT): bool
public thumbnailImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $fill = false,    bool $legacy = false): bool
public tintImage(mixed $tint, mixed $opacity, bool $legacy = false): bool
public __toString(): string
public transformImage(string $crop, string $geometry): Imagick
public transformImageColorspace(int $colorspace): bool
public transparentPaintImage(    mixed $target,    float $alpha,    float $fuzz,    bool $invert): bool
public transposeImage(): bool
public transverseImage(): bool
public trimImage(float $fuzz): bool
public uniqueImageColors(): bool
public unsharpMaskImage(    float $radius,    float $sigma,    float $amount,    float $threshold,    int $channel = Imagick::CHANNEL_DEFAULT): bool
public valid(): bool
public vignetteImage(    float $blackPoint,    float $whitePoint,    int $x,    int $y): bool
public waveImage(float $amplitude, float $length): bool
public whiteThresholdImage(mixed $threshold): bool
public writeImage(string $filename = NULL): bool
public writeImageFile(resource $filehandle, string $format = ?): bool
public writeImages(string $filename, bool $adjoin): bool
public writeImagesFile(resource $filehandle, string $format = ?): bool

   }
```

## Методи зображення та глобальні методи

Клас Imagick має можливість утримувати та обробляти кілька зображень одночасно. Це досягається рахунок внутрішнього стека, у якому існує покажчик, що вказує на поточне зображення. Деякі функції працюють з усіма зображеннями в класі Imagick, але все-таки більшість працює тільки з поточним зображенням у внутрішньому стеку. За згодою, імена методів можуть містити слово Image для позначення того, що вони впливають лише на поточне зображення у стеку.

## Методи класу

Тут наведено список найбільш використовуваних методів, об'єднаних у групи за призначенням:

**Методи класу за призначенням**

| Эффекты изображения                                                      | Методы получения                                                                 | Методы установки                                                                 | Чтение/запись изображений                                    | Другие                                                           |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------|
| [Imagick::adaptiveBlurImage()](imagick.adaptiveblurimage.html)           | [Imagick::getCompression()](imagick.getcompression.html)                         | [Imagick::setBackgroundColor()](imagick.setbackgroundcolor.html)                 | [Imagick::construct()](imagick.construct.html)               | [Imagick::clear()](imagick.clear.html)                           |
| [Imagick::adaptiveResizeImage()](imagick.adaptiveresizeimage.html)       | [Imagick::getFilename()](imagick.getfilename.html)                               | [Imagick::setCompressionQuality()](imagick.setcompressionquality.html)           | [Imagick::addImage()](imagick.addimage.html)                 | [Imagick::clone()](imagick.clone.html)                           |
| [Imagick::adaptiveSharpenImage()](imagick.adaptivesharpenimage.html)     | [Imagick::getFormat()](imagick.getformat.html)                                   | [Imagick::setCompression()](imagick.setcompression.html)                         | [Imagick::appendImages()](imagick.appendimages.html)         | [Imagick::current()](imagick.current.html)                       |
| [Imagick::adaptiveThresholdImage()](imagick.adaptivethresholdimage.html) | [Imagick::getImageBackgroundColor()](imagick.getimagebackgroundcolor.html)       | [Imagick::setFilename()](imagick.setfilename.html)                               | [Imagick::getFilename()](imagick.getfilename.html)           | [Imagick::destroy()](imagick.destroy.html)                       |
| [Imagick::addNoiseImage()](imagick.addnoiseimage.html)                   | [Imagick::getImageBlob()](imagick.getimageblob.html)                             | [Imagick::getImagesBlob()](imagick.getimagesblob.html)                           | [Imagick::setFormat()](imagick.setformat.html)               | [Imagick::getFormat()](imagick.getformat.html)                   |
| [Imagick::affinetransformimage()](imagick.affinetransformimage.html)     | [Imagick::getImageBluePrimary()](imagick.getimageblueprimary.html)               | [Imagick::setImageBackgroundColor()](imagick.setimagebackgroundcolor.html)       | [Imagick::getImageFilename()](imagick.getimagefilename.html) | [Imagick::getHomeURL()](imagick.gethomeurl.html)                 |
| [Imagick::annotateImage()](imagick.annotateimage.html)                   | [Imagick::getImageBorderColor()](imagick.getimagebordercolor.html)               | [Imagick::setFirstIterator()](imagick.setfirstiterator.html)                     | [Imagick::getImageFormat()](imagick.getimageformat.html)     | [Imagick::commentImage()](imagick.commentimage.html)             |
| [Imagick::averageImages()](imagick.averageimages.html)                   | [Imagick::getImageChannelDepth()](imagick.getimagechanneldepth.html)             | [Imagick::setImageBias()](imagick.setimagebias.html)                             | [Imagick::getImage()](imagick.getimage.html)                 | [Imagick::getNumberImages()](imagick.getnumberimages.html)       |
| [Imagick::blackThresholdImage()](imagick.blackthresholdimage.html)       | [Imagick::getImageChannelDistortion()](imagick.getimagechanneldistortion.html)   | [Imagick::setImageBluePrimary()](imagick.setimageblueprimary.html)               | [Imagick::setImageFilename()](imagick.setimagefilename.html) | [Imagick::getReleaseDate()](imagick.getreleasedate.html)         |
| [Imagick::blurImage()](imagick.blurimage.html)                           | [Imagick::getImageChannelExtrema()](imagick.getimagechannelextrema.html)         | [Imagick::setImageBorderColor()](imagick.setimagebordercolor.html)               | [Imagick::setImageFormat()](imagick.setimageformat.html)     | [Imagick::getVersion()](imagick.getversion.html)                 |
| [Imagick::borderImage()](imagick.borderimage.html)                       | [Imagick::getImageChannelMean()](imagick.getimagechannelmean.html)               | [Imagick::setImageChannelDepth()](imagick.setimagechanneldepth.html)             | [Imagick::readImageFile()](imagick.readimagefile.html)       | [Imagick::hasNextImage()](imagick.hasnextimage.html)             |
| [Imagick::charcoalImage()](imagick.charcoalimage.html)                   | [Imagick::getImageChannelStatistics()](imagick.getimagechannelstatistics.html)   | [Imagick::setImageColormapColor()](imagick.setimagecolormapcolor.html)           | [Imagick::readImage()](imagick.readimage.html)               | [Imagick::hasPreviousImage()](imagick.haspreviousimage.html)     |
| [Imagick::chopImage()](imagick.chopimage.html)                           | [Imagick::getImageColormapColor()](imagick.getimagecolormapcolor.html)           | [Imagick::setImageColorSpace()](imagick.setimagecolorspace.html)                 | [Imagick::writeImages()](imagick.writeimages.html)           | [Imagick::labelImage()](imagick.labelimage.html)                 |
| [Imagick::clipImage()](imagick.clipimage.html)                           | [Imagick::getImageColorspace()](imagick.getimagecolorspace.html)                 | [Imagick::setImageCompose()](imagick.setimagecompose.html)                       | [Imagick::writeImage()](imagick.writeimage.html)             | [Imagick::newImage()](imagick.newimage.html)                     |
| [Imagick::clipPathImage()](imagick.clippathimage.html)                   | [Imagick::getImageColors()](imagick.getimagecolors.html)                         | [Imagick::setImageCompression()](imagick.setimagecompression.html)               |                                                              | [Imagick::newPseudoImage()](imagick.newpseudoimage.html)         |
| [Imagick::coalesceImages()](imagick.coalesceimages.html)                 | [Imagick::getImageCompose()](imagick.getimagecompose.html)                       | [Imagick::setImageDelay()](imagick.setimagedelay.html)                           |                                                              | [Imagick::nextImage()](imagick.nextimage.html)                   |
| [Imagick::colorFloodFillImage()](imagick.colorfloodfillimage.html)       | [Imagick::getImageDelay()](imagick.getimagedelay.html)                           | [Imagick::setImageDepth()](imagick.setimagedepth.html)                           |                                                              | [Imagick::pingImageBlob()](imagick.pingimageblob.html)           |
| [Imagick::colorizeImage()](imagick.colorizeimage.html)                   | [Imagick::getImageDepth()](imagick.getimagedepth.html)                           | [Imagick::setImageDispose()](imagick.setimagedispose.html)                       |                                                              | [Imagick::pingImageFile()](imagick.pingimagefile.html)           |
| [Imagick::combineImages()](imagick.combineimages.html)                   | [Imagick::getImageDispose()](imagick.getimagedispose.html)                       | [Imagick::setImageDispose()](imagick.setimagedispose.html)                       |                                                              | [Imagick::pingImage()](imagick.pingimage.html)                   |
| [Imagick::compareImageChannels()](imagick.compareimagechannels.html)     | [Imagick::getImageDistortion()](imagick.getimagedistortion.html)                 | [Imagick::setImageExtent()](imagick.setimageextent.html)                         |                                                              | [Imagick::previousImage()](imagick.previousimage.html)           |
| [Imagick::compareImageLayers()](imagick.compareimagelayers.html)         | [Imagick::getImageExtrema()](imagick.getimageextrema.html)                       | [Imagick::setImageFilename()](imagick.setimagefilename.html)                     |                                                              | [Imagick::profileImage()](imagick.profileimage.html)             |
| [Imagick::compositeImage()](imagick.compositeimage.html)                 | [Imagick::getImageFilename()](imagick.getimagefilename.html)                     | [Imagick::setImageFormat()](imagick.setimageformat.html)                         |                                                              | [Imagick::queryFormats()](imagick.queryformats.html)             |
| [Imagick::contrastImage()](imagick.contrastimage.html)                   | [Imagick::getImageFormat()](imagick.getimageformat.html)                         | [Imagick::setImageGamma()](imagick.setimagegamma.html)                           |                                                              | [Imagick::removeImageProfile()](imagick.removeimageprofile.html) |
| [Imagick::contrastStretchImage()](imagick.contraststretchimage.html)     | [Imagick::getImageGamma()](imagick.getimagegamma.html)                           | [Imagick::setImageGreenPrimary()](imagick.setimagegreenprimary.html)             |                                                              | [Imagick::removeImage()](imagick.removeimage.html)               |
| [Imagick::convolveImage()](imagick.convolveimage.html)                   | [Imagick::getImageGeometry()](imagick.getimagegeometry.html)                     | [Imagick::setImageIndex()](imagick.setimageindex.html)                           |                                                              | [Imagick::setFirstIterator()](imagick.setfirstiterator.html)     |
| [Imagick::cropImage()](imagick.cropimage.html)                           | [Imagick::getImageGreenPrimary()](imagick.getimagegreenprimary.html)             | [Imagick::setImageInterpolateMethod()](imagick.setimageinterpolatemethod.html)   |                                                              | [Imagick::setImageIndex()](imagick.setimageindex.html)           |
| [Imagick::cycleColormapImage()](imagick.cyclecolormapimage.html)         | [Imagick::getImageHeight()](imagick.getimageheight.html)                         | [Imagick::setImageIterations()](imagick.setimageiterations.html)                 |                                                              | [Imagick::valid()](imagick.valid.html)                           |
| [Imagick::deconstructImages()](imagick.deconstructimages.html)           | [Imagick::getImageHistogram()](imagick.getimagehistogram.html)                   | [Imagick::setImageMatteColor()](imagick.setimagemattecolor.html)                 |                                                              | [Imagick::getCopyright()](imagick.getcopyright.html)             |
| [Imagick::drawImage()](imagick.drawimage.html)                           | [Imagick::getImageIndex()](imagick.getimageindex.html)                           | [Imagick::setImageMatte()](imagick.setimagematte.html)                           |                                                              |                                                                  |
| [Imagick::edgeImage()](imagick.edgeimage.html)                           | [Imagick::getImageInterlaceScheme()](imagick.getimageinterlacescheme.html)       | [Imagick::setImagePage()](imagick.setimagepage.html)                             |                                                              |                                                                  |
| [Imagick::embossImage()](imagick.embossimage.html)                       | [Imagick::getImageInterpolateMethod()](imagick.getimageinterpolatemethod.html)   | [Imagick::setImageProfile()](imagick.setimageprofile.html)                       |                                                              |                                                                  |
| [Imagick::enhanceImage()](imagick.enhanceimage.html)                     | [Imagick::getImageIterations()](imagick.getimageiterations.html)                 | [Imagick::setImageProperty()](imagick.setimageproperty.html)                     |                                                              |                                                                  |
| [Imagick::equalizeImage()](imagick.equalizeimage.html)                   | [Imagick::getImageMatteColor()](imagick.getimagemattecolor.html)                 | [Imagick::setImageRedPrimary()](imagick.setimageredprimary.html)                 |                                                              |                                                                  |
| [Imagick::evaluateImage()](imagick.evaluateimage.html)                   | [Imagick::getImageMatte()](imagick.getimagematte.html)                           | [Imagick::setImageRenderingIntent()](imagick.setimagerenderingintent.html)       |                                                              |                                                                  |
| [Imagick::flattenImages()](imagick.flattenimages.html)                   | [Imagick::getImagePage()](imagick.getimagepage.html)                             | [Imagick::setImageResolution()](imagick.setimageresolution.html)                 |                                                              |                                                                  |
| [Imagick::flipImage()](imagick.flipimage.html)                           | [Imagick::getImagePixelColor()](imagick.getimagepixelcolor.html)                 | [Imagick::setImageScene()](imagick.setimagescene.html)                           |                                                              |                                                                  |
| [Imagick::flopImage()](imagick.flopimage.html)                           | [Imagick::getImageProfile()](imagick.getimageprofile.html)                       | [Imagick::setImageTicksPerSecond()](imagick.setimagetickspersecond.html)         |                                                              |                                                                  |
|                                                                          | [Imagick::getImageProperty()](imagick.getimageproperty.html)                     | [Imagick::setImageType()](imagick.setimagetype.html)                             |                                                              |                                                                  |
| [Imagick::fxImage()](imagick.fximage.html)                               | [Imagick::getImageRedPrimary()](imagick.getimageredprimary.html)                 | [Imagick::setImageUnits()](imagick.setimageunits.html)                           |                                                              |                                                                  |
| [Imagick::gammaImage()](imagick.gammaimage.html)                         | [Imagick::getImageRegion()](imagick.getimageregion.html)                         | [Imagick::setImageVirtualPixelMethod()](imagick.setimagevirtualpixelmethod.html) |                                                              |                                                                  |
| [Imagick::gaussianBlurImage()](imagick.gaussianblurimage.html)           | [Imagick::getImageRenderingIntent()](imagick.getimagerenderingintent.html)       | [Imagick::setImageWhitepoint()](imagick.setimagewhitepoint.html)                 |                                                              |                                                                  |
| [Imagick::implodeImage()](imagick.implodeimage.html)                     | [Imagick::getImageResolution()](imagick.getimageresolution.html)                 | [Imagick::setInterlaceScheme()](imagick.setinterlacescheme.html)                 |                                                              |                                                                  |
| [Imagick::levelImage()](imagick.levelimage.html)                         | [Imagick::getImageScene()](imagick.getimagescene.html)                           | [Imagick::setOption()](imagick.setoption.html)                                   |                                                              |                                                                  |
| [Imagick::linearStretchImage()](imagick.linearstretchimage.html)         | [Imagick::getImageSignature()](imagick.getimagesignature.html)                   | [Imagick::setPage()](imagick.setpage.html)                                       |                                                              |                                                                  |
| [Imagick::magnifyImage()](imagick.magnifyimage.html)                     | [Imagick::getImageTicksPerSecond()](imagick.getimagetickspersecond.html)         | [Imagick::setResolution()](imagick.setresolution.html)                           |                                                              |                                                                  |
| [Imagick::matteFloodFillImage()](imagick.mattefloodfillimage.html)       | [Imagick::getImageTotalInkDensity()](imagick.getimagetotalinkdensity.html)       | [Imagick::setResourceLimit()](imagick.setresourcelimit.html)                     |                                                              |                                                                  |
| [Imagick::medianFilterImage()](imagick.medianfilterimage.html)           | [Imagick::getImageType()](imagick.getimagetype.html)                             | [Imagick::setSamplingFactors()](imagick.setsamplingfactors.html)                 |                                                              |                                                                  |
| [Imagick::minifyImage()](imagick.minifyimage.html)                       | [Imagick::getImageUnits()](imagick.getimageunits.html)                           | [Imagick::setSizeOffset()](imagick.setsizeoffset.html)                           |                                                              |                                                                  |
| [Imagick::modulateImage()](imagick.modulateimage.html)                   | [Imagick::getImageVirtualPixelMethod()](imagick.getimagevirtualpixelmethod.html) | [Imagick::setSize()](imagick.setsize.html)                                       |                                                              |                                                                  |
| [Imagick::montageImage()](imagick.montageimage.html)                     | [Imagick::getImageWhitepoint()](imagick.getimagewhitepoint.html)                 | [Imagick::setType()](imagick.settype.html)                                       |                                                              |                                                                  |
| [Imagick::morphImages()](imagick.morphimages.html)                       | [Imagick::getImageWidth()](imagick.getimagewidth.html)                           |                                                                                  |                                                              |                                                                  |
| [Imagick::mosaicImages()](imagick.mosaicimages.html)                     | [Imagick::getImage()](imagick.getimage.html)                                     |                                                                                  |                                                              |                                                                  |
| [Imagick::motionBlurImage()](imagick.motionblurimage.html)               | [Imagick::getInterlaceScheme()](imagick.getinterlacescheme.html)                 |                                                                                  |                                                              |                                                                  |
| [Imagick::negateImage()](imagick.negateimage.html)                       | [Imagick::getNumberImages()](imagick.getnumberimages.html)                       |                                                                                  |                                                              |                                                                  |
| [Imagick::normalizeImage()](imagick.normalizeimage.html)                 | [Imagick::getOption()](imagick.getoption.html)                                   |                                                                                  |                                                              |                                                                  |
| [Imagick::oilPaintImage()](imagick.oilpaintimage.html)                   | [Imagick::getPackageName()](imagick.getpackagename.html)                         |                                                                                  |                                                              |                                                                  |
| [Imagick::optimizeImageLayers()](imagick.optimizeimagelayers.html)       | [Imagick::getPage()](imagick.getpage.html)                                       |                                                                                  |                                                              |                                                                  |
| [Imagick::paintOpaqueImage()](imagick.paintopaqueimage.html)             | [Imagick::getPixelIterator()](imagick.getpixeliterator.html)                     |                                                                                  |                                                              |                                                                  |
| [Imagick::paintTransparentImage()](imagick.painttransparentimage.html)   | [Imagick::getPixelRegionIterator()](imagick.getpixelregioniterator.html)         |                                                                                  |                                                              |                                                                  |
| [Imagick::posterizeImage()](imagick.posterizeimage.html)                 | [Imagick::getQuantumDepth()](imagick.getquantumdepth.html)                       |                                                                                  |                                                              |                                                                  |
| [Imagick::radialBlurImage()](imagick.radialblurimage.html)               | [Imagick::getQuantumRange()](imagick.getquantumrange.html)                       |                                                                                  |                                                              |                                                                  |
| [Imagick::raiseImage()](imagick.raiseimage.html)                         | [Imagick::getResourceLimit()](imagick.getresourcelimit.html)                     |                                                                                  |                                                              |                                                                  |
| [Imagick::randomThresholdImage()](imagick.randomthresholdimage.html)     | [Imagick::getResource()](imagick.getresource.html)                               |                                                                                  |                                                              |                                                                  |
| [Imagick::reduceNoiseImage()](imagick.reducenoiseimage.html)             | [Imagick::getSamplingFactors()](imagick.getsamplingfactors.html)                 |                                                                                  |                                                              |                                                                  |
| [Imagick::render()](imagick.render.html)                                 | [Imagick::getSizeOffset()](imagick.getsizeoffset.html)                           |                                                                                  |                                                              |                                                                  |
| [Imagick::resampleImage()](imagick.resampleimage.html)                   | [Imagick::getSize()](imagick.getsize.html)                                       |                                                                                  |                                                              |                                                                  |
| [Imagick::resizeImage()](imagick.resizeimage.html)                       | [Imagick::identifyImage()](imagick.identifyimage.html)                           |                                                                                  |                                                              |                                                                  |
| [Imagick::rollImage()](imagick.rollimage.html)                           | [Imagick::getImageSize()](imagick.getimagesize.html)                             |                                                                                  |                                                              |                                                                  |
| [Imagick::rotateImage()](imagick.rotateimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::sampleImage()](imagick.sampleimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::scaleImage()](imagick.scaleimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::separateImageChannel()](imagick.separateimagechannel.html)     |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::sepiaToneImage()](imagick.sepiatoneimage.html)                 |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::shadeImage()](imagick.shadeimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::shadowImage()](imagick.shadowimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::sharpenImage()](imagick.sharpenimage.html)                     |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::shaveImage()](imagick.shaveimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::shearImage()](imagick.shearimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::sigmoidalContrastImage()](imagick.sigmoidalcontrastimage.html) |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::sketchImage()](imagick.sketchimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::solarizeImage()](imagick.solarizeimage.html)                   |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::spliceImage()](imagick.spliceimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::spreadImage()](imagick.spreadimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::steganoImage()](imagick.steganoimage.html)                     |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::stereoImage()](imagick.stereoimage.html)                       |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::stripImage()](imagick.stripimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::swirlImage()](imagick.swirlimage.html)                         |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::textureImage()](imagick.textureimage.html)                     |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::thresholdImage()](imagick.thresholdimage.html)                 |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::thumbnailImage()](imagick.thumbnailimage.html)                 |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::tintImage()](imagick.tintimage.html)                           |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::transverseImage()](imagick.transverseimage.html)               |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::trimImage()](imagick.trimimage.html)                           |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::uniqueImageColors()](imagick.uniqueimagecolors.html)           |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::unsharpMaskImage()](imagick.unsharpmaskimage.html)             |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::vignetteImage()](imagick.vignetteimage.html)                   |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::waveImage()](imagick.waveimage.html)                           |                                                                                  |                                                                                  |                                                              |                                                                  |
| [Imagick::whiteThresholdImage()](imagick.whitethresholdimage.html)       |                                                                                  |                                                                                  |                                                              |                                                                  |

## Зміст

-   [Imagick::adaptiveBlurImage](imagick.adaptiveblurimage.html) — Додає адаптивний фільтр розмиття до зображення
-   [Imagick::adaptiveResizeImage](imagick.adaptiveresizeimage.html) — Адаптивна зміна розміру зображення з даними тріангуляції
-   [Imagick::adaptiveSharpenImage](imagick.adaptivesharpenimage.html) — Адаптивна зміна різкості зображення
-   [Imagick::adaptiveThresholdImage](imagick.adaptivethresholdimage.html) — Вибір порога кожного пікселя в залежності від діапазону інтенсивності
-   [Imagick::addImage](imagick.addimage.html) — Додає нове зображення до списку зображень об'єкту Imagick
-   [Imagick::addNoiseImage](imagick.addnoiseimage.html) - Накладає випадковий шум на зображення
-   [Imagick::affineTransformImage](imagick.affinetransformimage.html) — Перетворення зображення
-   [Imagick::animateImages](imagick.animateimages.html) — Анімація одного або кількох зображень
-   [Imagick::annotateImage](imagick.annotateimage.html) — Додає текстовий коментар на зображення
-   [Imagick::appendImages](imagick.appendimages.html) — Об'єднує набір зображень
-   [Imagick::autoLevelImage](imagick.autolevelimage.html) - Опис
-   [Imagick::averageImages](imagick.averageimages.html) — Усереднює набір зображень
-   [Imagick::blackThresholdImage](imagick.blackthresholdimage.html) — Перевести всі пікселі нижче граничного значення в чорний колір
-   [Imagick::blueShiftImage](imagick.blueshiftimage.html) - Опис
-   [Imagick::blurImage](imagick.blurimage.html) — Додає фільтр розмиття до зображення
-   [Imagick::borderImage](imagick.borderimage.html) — Оточує зображення рамкою
-   [Imagick::brightnessContrastImage](imagick.brightnesscontrastimage.html) - Опис
-   [Imagick::charcoalImage](imagick.charcoalimage.html) - Малювання вугіллям
-   [Imagick::chopImage](imagick.chopimage.html) — Видаляє область зображення та обрізає його.
-   [Imagick::clampImage](imagick.clampimage.html) - Опис
-   [Imagick::clear](imagick.clear.html) — Очищає всі ресурси, пов'язані з об'єктом Imagick
-   [Imagick::clipImage](imagick.clipimage.html) — Обрізка вздовж найближчого контуру з профілем 8BIM
-   [Imagick::clipImagePath](imagick.clipimagepath.html) - Опис
-   [Imagick::clipPathImage](imagick.clippathimage.html) — Відсікти уздовж зазначеного контуру з профілем 8BIM
-   [Imagick::clone](imagick.clone.html) — Створює точну копію об'єкту Imagick
-   [Imagick::clutImage](imagick.clutimage.html) — Замінює кольори у зображенні
-   [Imagick::coalesceImages](imagick.coalesceimages.html) — Компонує набір зображень
-   [Imagick::colorFloodfillImage](imagick.colorfloodfillimage.html) — Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::colorizeImage](imagick.colorizeimage.html) — Змішування кольору заливки із зображенням
-   [Imagick::colorMatrixImage](imagick.colormatriximage.html) — Застосовує перетворення кольору до зображення
-   [Imagick::combineImages](imagick.combineimages.html) — Об'єднує одне або кілька зображень в одне зображення
-   [Imagick::commentImage](imagick.commentimage.html) — Додає коментар до вашого зображення
-   [Imagick::compareImageChannels](imagick.compareimagechannels.html) — Повертає різницю в одному чи кількох зображеннях
-   [Imagick::compareImageLayers](imagick.compareimagelayers.html) — Повертає максимальну область, що обмежує між зображеннями.
-   [Imagick::compareImages](imagick.compareimages.html) — Порівнює зображення з відновленим зображенням
-   [Imagick::compositeImage](imagick.compositeimage.html) — Накладає одне зображення на інше
-   [Imagick::construct](imagick.construct.html) - Конструктор об'єкту Imagick
-   [Imagick::contrastImage](imagick.contrastimage.html) — Змінює контраст зображення
-   [Imagick::contrastStretchImage](imagick.contraststretchimage.html) — Підвищує контрастність кольорового зображення
-   [Imagick::convolveImage](imagick.convolveimage.html) — Застосовує ядро ​​згортки до зображення.
-   [Imagick::count](imagick.count.html) — Отримує кількість зображень
-   [Imagick::cropImage](imagick.cropimage.html) — Витягує область зображення
-   [Imagick::cropThumbnailImage](imagick.cropthumbnailimage.html) - Створює обрізану мініатюру
-   [Imagick::current](imagick.current.html) — Повертає посилання на поточний об'єкт Imagick
-   [Imagick::cycleColormapImage](imagick.cyclecolormapimage.html) — Відображає карту кольорів зображення
-   [Imagick::decipherImage](imagick.decipherimage.html) — Розшифровує зображення
-   [Imagick::deconstructImages](imagick.deconstructimages.html) — Повертає певні піксельні відмінності між зображеннями
-   [Imagick::deleteImageArtifact](imagick.deleteimageartifact.html) — Видаляє артефакт зображення
-   [Imagick::deleteImageProperty](imagick.deleteimageproperty.html) - Опис
-   [Imagick::deskewImage](imagick.deskewimage.html) — Видаляє перекіс із зображення
-   [Imagick::despeckleImage](imagick.despeckleimage.html) - Зменшує спекл-шум на зображенні
-   [Imagick::destroy](imagick.destroy.html) — Видаляє об'єкт Imagick
-   [Imagick::displayImage](imagick.displayimage.html) — Виводить зображення
-   [Imagick::displayImages](imagick.displayimages.html) — Виводить зображення або послідовність зображень
-   [Imagick::distortImage](imagick.distortimage.html) — Спотворює зображення, використовуючи різні методи спотворення
-   [Imagick::drawImage](imagick.drawimage.html) — Виконує рендеринг об'єкту ImagickDraw на поточному зображенні
-   [Imagick::edgeImage](imagick.edgeimage.html) — Підсилює краї зображення.
-   [Imagick::embossImage](imagick.embossimage.html) — Повертає зображення у градаціях сірого із тривимірним ефектом
-   [Imagick::encipherImage](imagick.encipherimage.html) - Шифрує зображення
-   [Imagick::enhanceImage](imagick.enhanceimage.html) — Покращує якість шумного зображення
-   [Imagick::equalizeImage](imagick.equalizeimage.html) — Вирівнює гістограму зображення
-   [Imagick::evaluateImage](imagick.evaluateimage.html) — Застосовує вираз до зображення
-   [Imagick::exportImagePixels](imagick.exportimagepixels.html) — Експортує пікселі зображення
-   [Imagick::extentImage](imagick.extentimage.html) — Встановлює розмір зображення
-   [Imagick::filter](imagick.filter.html) - Опис
-   [Imagick::flattenImages](imagick.flattenimages.html) — Поєднує послідовність зображень
-   [Imagick::flipImage](imagick.flipimage.html) — Створює вертикальне дзеркало зображення
-   [Imagick::floodFillPaintImage](imagick.floodfillpaintimage.html) — Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::flopImage](imagick.flopimage.html) — Створює горизонтальне дзеркальне відображення
-   [Imagick::forwardFourierTransformImage](imagick.forwardfouriertransformimage.html) - Опис
-   [Imagick::frameImage](imagick.frameimage.html) — Додає імітацію тривимірного кордону
-   [Imagick::functionImage](imagick.functionimage.html) — Застосовує функцію зображення.
-   [Imagick::fxImage](imagick.fximage.html) — Оцінює вираз для кожного пікселя у зображенні
-   [Imagick::gammaImage](imagick.gammaimage.html) - Гамма-корекція зображення
-   [Imagick::gaussianBlurImage](imagick.gaussianblurimage.html) — Розмиває зображення
-   [Imagick::getColorspace](imagick.getcolorspace.html) — Повертає палітру кольорів
-   [Imagick::getCompression](imagick.getcompression.html) — Повертає тип стиснення об'єкта
-   [Imagick::getCompressionQuality](imagick.getcompressionquality.html) — Повертає якість стиснення об'єкта
-   [Imagick::getCopyright](imagick.getcopyright.html) — Повертає копірайт API ImageMagick у вигляді рядка
-   [Imagick::getFilename](imagick.getfilename.html) - Ім'я файлу результуючого зображення
-   [Imagick::getFont](imagick.getfont.html) — Повертає назву шрифту
-   [Imagick::getFormat](imagick.getformat.html) — Повертає формат Imagick об'єкту
-   [Imagick::getGravity](imagick.getgravity.html) - Повертає значення гравітації (тяжіння)
-   [Imagick::getHomeURL](imagick.gethomeurl.html) — Повертає домашню URL-адресу бібліотеки ImageMagick
-   [Imagick::getImage](imagick.getimage.html) — Повертає новий об'єкт Imagick
-   [Imagick::getImageAlphaChannel](imagick.getimagealphachannel.html) — Перевіряє, чи є зображення альфа-канал
-   [Imagick::getImageArtifact](imagick.getimageartifact.html) — Повертає артефакт зображення
-   [Imagick::getImageAttribute](imagick.getimageattribute.html) - Повертає іменований атрибут
-   [Imagick::getImageBackgroundColor](imagick.getimagebackgroundcolor.html) — Повертає колір тла зображення
-   [Imagick::getImageBlob](imagick.getimageblob.html) — Повертає послідовність зображень у вигляді BLOB
-   [Imagick::getImageBluePrimary](imagick.getimageblueprimary.html) — Повертає основну точку синього кольору зображення
-   [Imagick::getImageBorderColor](imagick.getimagebordercolor.html) — Повертає колір рамки зображення
-   [Imagick::getImageChannelDepth](imagick.getimagechanneldepth.html) — Повертає глибину для певного каналу зображення
-   [Imagick::getImageChannelDistortion](imagick.getimagechanneldistortion.html) — Порівнює канали зображення з відновленим зображенням
-   [Imagick::getImageChannelDistortions](imagick.getimagechanneldistortions.html) — Повертає спотворення каналу
-   [Imagick::getImageChannelExtrema](imagick.getimagechannelextrema.html) — Повертає екстремуми для одного або кількох каналів зображення
-   [Imagick::getImageChannelKurtosis](imagick.getimagechannelkurtosis.html) — Повертає ексцес та асиметрію певного каналу
-   [Imagick::getImageChannelMean](imagick.getimagechannelmean.html) — Повертає середнє та стандартне відхилення
-   [Imagick::getImageChannelRange](imagick.getimagechannelrange.html) — Повертає діапазон каналів
-   [Imagick::getImageChannelStatistics](imagick.getimagechannelstatistics.html) — Повертає статистику для кожного каналу зображення
-   [Imagick::getImageClipMask](imagick.getimageclipmask.html) — Повертає відсічну маску зображення
-   [Imagick::getImageColormapColor](imagick.getimagecolormapcolor.html) — Повертає колір зазначеного індексу палітри
-   [Imagick::getImageColors](imagick.getimagecolors.html) — Повертає кількість унікальних кольорів у зображенні
-   [Imagick::getImageColorspace](imagick.getimagecolorspace.html) — Повертає палітру кольорів зображення
-   [Imagick::getImageCompose](imagick.getimagecompose.html) — Повертає складовий оператор, пов'язаний із зображенням
-   [Imagick::getImageCompression](imagick.getimagecompression.html) — Повертає поточний тип компресії зображення
-   [Imagick::getImageCompressionQuality](imagick.getimagecompressionquality.html) — Повертає поточну якість стиснення зображення
-   [Imagick::getImageDelay](imagick.getimagedelay.html) — Повертає затримку зображення
-   [Imagick::getImageDepth](imagick.getimagedepth.html) — Повертає глибину зображення
-   [Imagick::getImageDispose](imagick.getimagedispose.html) — Повертає метод видалення зображення
-   [Imagick::getImageDistortion](imagick.getimagedistortion.html) — Порівнює зображення з відновленим зображенням
-   [Imagick::getImageExtrema](imagick.getimageextrema.html) — Повертає екстремуми зображення
-   [Imagick::getImageFilename](imagick.getimagefilename.html) — Повертає ім'я файлу конкретного зображення у послідовності
-   [Imagick::getImageFormat](imagick.getimageformat.html) — Повертає формат зображення в послідовності.
-   [Imagick::getImageGamma](imagick.getimagegamma.html) — Повертає гаму зображення
-   [Imagick::getImageGeometry](imagick.getimagegeometry.html) — Повертає ширину та висоту у вигляді асоціативного масиву
-   [Imagick::getImageGravity](imagick.getimagegravity.html) - Повертає значення гравітації (тяжіння)
-   [Imagick::getImageGreenPrimary](imagick.getimagegreenprimary.html) — Повертає первинну точку кольоровості зеленого
-   [Imagick::getImageHeight](imagick.getimageheight.html) — Повертає висоту зображення
-   [Imagick::getImageHistogram](imagick.getimagehistogram.html) — Повертає гістограму зображення
-   [Imagick::getImageIndex](imagick.getimageindex.html) — Повертає індекс активного поточного зображення.
-   [Imagick::getImageInterlaceScheme](imagick.getimageinterlacescheme.html) — Отримує схему надрядкового зображення
-   [Imagick::getImageInterpolateMethod](imagick.getimageinterpolatemethod.html) — Повертає метод інтерполяції
-   [Imagick::getImageIterations](imagick.getimageiterations.html) — Повертає ітерацію зображення
-   [Imagick::getImageLength](imagick.getimagelength.html) — Повертає довжину зображення у байтах
-   [Imagick::getImageMatte](imagick.getimagematte.html) — Повертає, якщо зображення містить матовий канал
-   [Imagick::getImageMatteColor](imagick.getimagemattecolor.html) — Повертає матовий колір зображення
-   [Imagick::getImageMimeType](imagick.getimagemimetype.html) — Повертає MIME-тип зображення
-   [Imagick::getImageOrientation](imagick.getimageorientation.html) — Повертає орієнтацію зображення
-   [Imagick::getImagePage](imagick.getimagepage.html) — Повертає геометрію сторінки
-   [Imagick::getImagePixelColor](imagick.getimagepixelcolor.html) — Повертає колір вказаного пікселя
-   [Imagick::getImageProfile](imagick.getimageprofile.html) — Повертає іменований профіль зображення
-   [Imagick::getImageProfiles](imagick.getimageprofiles.html) — Повертає профілі зображень
-   [Imagick::getImageProperties](imagick.getimageproperties.html) — Повертає властивості зображення
-   [Imagick::getImageProperty](imagick.getimageproperty.html) — Повертає іменовану властивість зображення
-   [Imagick::getImageRedPrimary](imagick.getimageredprimary.html) — Повертає червону первинну точку кольоровості
-   [Imagick::getImageRegion](imagick.getimageregion.html) — Витягує область зображення
-   [Imagick::getImageRenderingIntent](imagick.getimagerenderingintent.html) — Повертає схему передачі кольору зображення
-   [Imagick::getImageResolution](imagick.getimageresolution.html) — Повертає роздільну здатність зображення за X та Y
-   [Imagick::getImagesBlob](imagick.getimagesblob.html) — Повертає всі послідовності зображення у вигляді великого двійкового об'єкта
-   [Imagick::getImageScene](imagick.getimagescene.html) — Повертає сцену зображення
-   [Imagick::getImageSignature](imagick.getimagesignature.html) - Генерує хеш SHA-256
-   [Imagick::getImageSize](imagick.getimagesize.html) — Повертає розмір зображення у байтах
-   [Imagick::getImageTicksPerSecond](imagick.getimagetickspersecond.html) — Отримує кількість кадрів на секунду для зображення
-   [Imagick::getImageTotalInkDensity](imagick.getimagetotalinkdensity.html) — Повертає загальну щільність чорнила зображення
-   [Imagick::getImageType](imagick.getimagetype.html) — Повертає можливий тип зображення
-   [Imagick::getImageUnits](imagick.getimageunits.html) — Повертає одиниці вимірювання роздільної здатності зображення
-   [Imagick::getImageVirtualPixelMethod](imagick.getimagevirtualpixelmethod.html) — Повертає метод віртуального пікселя
-   [Imagick::getImageWhitePoint](imagick.getimagewhitepoint.html) — Повертає білу точку кольоровості
-   [Imagick::getImageWidth](imagick.getimagewidth.html) — Повертає ширину зображення
-   [Imagick::getInterlaceScheme](imagick.getinterlacescheme.html) — Отримує схему стиснення зображення
-   [Imagick::getIteratorIndex](imagick.getiteratorindex.html) — Повертає індекс активного поточного зображення.
-   [Imagick::getNumberImages](imagick.getnumberimages.html) — Повертає кількість зображень в об'єкті
-   [Imagick::getOption](imagick.getoption.html) — Повертає значення, пов'язане із зазначеним ключем
-   [Imagick::getPackageName](imagick.getpackagename.html) — Повертає ім'я ImageMagick
-   [Imagick::getPage](imagick.getpage.html) — Повертає геометрію сторінки
-   [Imagick::getPixelIterator](imagick.getpixeliterator.html) - Повертає MagickPixelIterator
-   [Imagick::getPixelRegionIterator](imagick.getpixelregioniterator.html) — Повертає об'єкт ImagickPixelIterator для секції зображення
-   [Imagick::getPointSize](imagick.getpointsize.html) — Повертає розмір точки
-   [Imagick::getQuantum](imagick.getquantum.html) — Повертає квантовий діапазон ImageMagick
-   [Imagick::getQuantumDepth](imagick.getquantumdepth.html) - Повертає величину глибини
-   [Imagick::getQuantumRange](imagick.getquantumrange.html) — Повертає розмір спектру Imagick
-   [Imagick::getRegistry](imagick.getregistry.html) - Опис
-   [Imagick::getReleaseDate](imagick.getreleasedate.html) — Повертає дату випуску ImageMagick
-   [Imagick::getResource](imagick.getresource.html) — Повертає розмір пам'яті вказаного ресурсу.
-   [Imagick::getResourceLimit](imagick.getresourcelimit.html) — Повертає заданий ліміт ресурсів
-   [Imagick::getSamplingFactors](imagick.getsamplingfactors.html) — Повертає горизонтальний та вертикальний фактор вибірки
-   [Imagick::getSize](imagick.getsize.html) — Повертає розмір, пов'язаний із об'єктом Imagick
-   [Imagick::getSizeOffset](imagick.getsizeoffset.html) — Повертає розмір усунення
-   [Imagick::getVersion](imagick.getversion.html) — Повертає версію API ImageMagick
-   [Imagick::haldClutImage](imagick.haldclutimage.html) — Замінює кольори у зображенні
-   [Imagick::hasNextImage](imagick.hasnextimage.html) — Перевіряє, чи об'єкт містить більше зображень
-   [Imagick::hasPreviousImage](imagick.haspreviousimage.html) — Перевіряє, чи об'єкт має попереднє зображення.
-   [Imagick::identifyFormat](imagick.identifyformat.html) - Опис
-   [Imagick::identifyImage](imagick.identifyimage.html) — Визначає зображення та отримує атрибути
-   [Imagick::implodeImage](imagick.implodeimage.html) — Створює копію зображення
-   [Imagick::importImagePixels](imagick.importimagepixels.html) — Імпортує пікселі зображення
-   [Imagick::inverseFourierTransformImage](imagick.inversefouriertransformimage.html) - Реалізує дискретне перетворення Фур'є
-   [Imagick::labelImage](imagick.labelimage.html) — Додає позначку до зображення
-   [Imagick::levelImage](imagick.levelimage.html) — Регулює рівні зображення
-   [Imagick::linearStretchImage](imagick.linearstretchimage.html) — Розтягує з насиченням яскравість зображення
-   [Imagick::liquidRescaleImage](imagick.liquidrescaleimage.html) — Анімує зображення чи зображення
-   [Imagick::listRegistry](imagick.listregistry.html) - Опис
-   [Imagick::magnifyImage](imagick.magnifyimage.html) — Пропорційно масштабує зображення вдвічі
-   [Imagick::mapImage](imagick.mapimage.html) — Замінює кольори зображення на найближчий колір із еталонного зображення
-   [Imagick::matteFloodfillImage](imagick.mattefloodfillimage.html) — Змінює значення прозорості кольору
-   [Imagick::medianFilterImage](imagick.medianfilterimage.html) — Застосовує цифровий фільтр
-   [Imagick::mergeImageLayers](imagick.mergeimagelayers.html) — Об'єднує шари зображення
-   [Imagick::minifyImage](imagick.minifyimage.html) — Масштабує зображення пропорційно до половини його розміру.
-   [Imagick::modulateImage](imagick.modulateimage.html) — Керуйте яскравістю, насиченістю та відтінком
-   [Imagick::montageImage](imagick.montageimage.html) — Створює складне зображення
-   [Imagick::morphImages](imagick.morphimages.html) — Перетворює набір зображень
-   [Imagick::morphology](imagick.morphology.html) - Опис
-   [Imagick::mosaicImages](imagick.mosaicimages.html) — Формує мозаїку із зображень
-   [Imagick::motionBlurImage](imagick.motionblurimage.html) — Імітує розмиття у русі
-   [Imagick::negateImage](imagick.negateimage.html) - Інвертує кольори в еталонному зображенні
-   [Imagick::newImage](imagick.newimage.html) — Створює нове зображення
-   [Imagick::newPseudoImage](imagick.newpseudoimage.html) — Створює нове зображення
-   [Imagick::nextImage](imagick.nextimage.html) — Переходить до наступного зображення
-   [Imagick::normalizeImage](imagick.normalizeimage.html) — Підвищує контрастність кольорового зображення
-   [Imagick::oilPaintImage](imagick.oilpaintimage.html) — Імітує картину олією
-   [Imagick::opaquePaintImage](imagick.opaquepaintimage.html) — Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::optimizeImageLayers](imagick.optimizeimagelayers.html) — Видаляє повторювані частини зображень для оптимізації
-   [Imagick::orderedPosterizeImage](imagick.orderedposterizeimage.html) - Виконує впорядкований дизеринг
-   [Imagick::paintFloodfillImage](imagick.paintfloodfillimage.html) — Змінює значення кольору будь-якого пікселя, що відповідає меті
-   [Imagick::paintOpaqueImage](imagick.paintopaqueimage.html) — Змінює будь-який піксель, що відповідає кольору
-   [Imagick::paintTransparentImage](imagick.painttransparentimage.html) — Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою
-   [Imagick::pingImage](imagick.pingimage.html) — Отримує основні атрибути зображення
-   [Imagick::pingImageBlob](imagick.pingimageblob.html) — Швидко витягує атрибути
-   [Imagick::pingImageFile](imagick.pingimagefile.html) — Отримує базові атрибути зображення у спрощений спосіб.
-   [Imagick::polaroidImage](imagick.polaroidimage.html) - Імітує фото Polaroid
-   [Imagick::posterizeImage](imagick.posterizeimage.html) — Зменшує зображення до обмеженої кількості рівнів кольору
-   [Imagick::previewImages](imagick.previewimages.html) — Швидке визначення відповідних параметрів для обробки зображень
-   [Imagick::previousImage](imagick.previousimage.html) — Перехід до попереднього зображення в об'єкті
-   [Imagick::profileImage](imagick.profileimage.html) — Додає або видаляє профіль зображення
-   [Imagick::quantizeImage](imagick.quantizeimage.html) - Аналізує кольори еталонного зображення
-   [Imagick::quantizeImages](imagick.quantizeimages.html) — Аналізує кольори у послідовності зображень
-   [Imagick::queryFontMetrics](imagick.queryfontmetrics.html) — Повертає масив, який представляє метрики шрифту
-   [Imagick::queryFonts](imagick.queryfonts.html) — Повертає налаштовані шрифти
-   [Imagick::queryFormats](imagick.queryformats.html) — Повертає формати, які підтримує Imagick
-   [Imagick::radialBlurImage](imagick.radialblurimage.html) — Радіальне розмиття зображення
-   [Imagick::raiseImage](imagick.raiseimage.html) — Створює імітацію ефекту 3D-кнопки
-   [Imagick::randomThresholdImage](imagick.randomthresholdimage.html) — Створює висококонтрастне двокольорове зображення
-   [Imagick::readImage](imagick.readimage.html) — Читає зображення із файлу
-   [Imagick::readImageBlob](imagick.readimageblob.html) — Зчитує зображення з двійкового рядка
-   [Imagick::readImageFile](imagick.readimagefile.html) — Читає зображення із відкритого дескриптора файлу
-   [Imagick::readimages](imagick.readimages.html) — Читає зображення з масиву імен файлів
-   [Imagick::recolorImage](imagick.recolorimage.html) — Перефарбовує зображення
-   [Imagick::reduceNoiseImage](imagick.reducenoiseimage.html) — Згладжує контури зображення
-   [Imagick::remapImage](imagick.remapimage.html) — Перезначає кольори зображення
-   [Imagick::removeImage](imagick.removeimage.html) — Видалення зображення зі списку зображень
-   [Imagick::removeImageProfile](imagick.removeimageprofile.html) — Видаляє іменований профіль зображення та повертає його
-   [Imagick::render](imagick.render.html) - Відображає всі попередні команди малювання
-   [Imagick::resampleImage](imagick.resampleimage.html) — Перетворює зображення до бажаного дозволу
-   [Imagick::resetImagePage](imagick.resetimagepage.html) — Скидає сторінку зображення
-   [Imagick::resizeImage](imagick.resizeimage.html) — Масштабує зображення
-   [Imagick::rollImage](imagick.rollimage.html) — Зміщує зображення
-   [Imagick::rotateImage](imagick.rotateimage.html) — Повертає зображення
-   [Imagick::rotationalBlurImage](imagick.rotationalblurimage.html) — Застосовує обертальне розмиття до зображення.
-   [Imagick::roundCorners](imagick.roundcorners.html) — Заокруглює кути зображення
-   [Imagick::sampleImage](imagick.sampleimage.html) — Масштабує зображення з піксельною вибіркою
-   [Imagick::scaleImage](imagick.scaleimage.html) — Масштабує розмір зображення
-   [Imagick::segmentImage](imagick.segmentimage.html) — Сегментує зображення
-   [Imagick::selectiveBlurImage](imagick.selectiveblurimage.html) - Опис
-   [Imagick::separateImageChannel](imagick.separateimagechannel.html) — Відокремлює канал від зображення.
-   [Imagick::sepiaToneImage](imagick.sepiatoneimage.html) — Тонування зображення сепією
-   [Imagick::setBackgroundColor](imagick.setbackgroundcolor.html) — Встановлює колір тла об'єкта за промовчанням
-   [Imagick::setColorspace](imagick.setcolorspace.html) — Встановлює колірний простір
-   [Imagick::setCompression](imagick.setcompression.html) — Встановлює тип стиснення об'єкта за промовчанням
-   [Imagick::setCompressionQuality](imagick.setcompressionquality.html) — Встановлює якість стандартного стиснення об'єкта
-   [Imagick::setFilename](imagick.setfilename.html) — Встановлює ім'я файлу перед читанням чи записом зображення
-   [Imagick::setFirstIterator](imagick.setfirstiterator.html) - Встановлює ітератор Imagick для першого зображення
-   [Imagick::setFont](imagick.setfont.html) - Встановлює шрифт
-   [Imagick::setFormat](imagick.setformat.html) — Встановлює формат об'єкту Imagick
-   [Imagick::setGravity](imagick.setgravity.html) - Встановлює гравітацію
-   [Imagick::setImage](imagick.setimage.html) — Замінює зображення в об'єкті
-   [Imagick::setImageAlphaChannel](imagick.setimagealphachannel.html) - Встановлює альфа-канал зображення
-   [Imagick::setImageArtifact](imagick.setimageartifact.html) - Встановлює артефакт зображення
-   [Imagick::setImageAttribute](imagick.setimageattribute.html) — Встановлює атрибут зображення
-   [Imagick::setImageBackgroundColor](imagick.setimagebackgroundcolor.html) — Встановлює колір тла зображення
-   [Imagick::setImageBias](imagick.setimagebias.html) — Встановлює зміщення зображення для будь-якого методу, який згортає зображення
-   [Imagick::setImageBiasQuantum](imagick.setimagebiasquantum.html) - Опис
-   [Imagick::setImageBluePrimary](imagick.setimageblueprimary.html) — Встановлює кольоровість зображення блакитною основною точкою.
-   [Imagick::setImageBorderColor](imagick.setimagebordercolor.html) — Встановлює колір рамки зображення
-   [Imagick::setImageChannelDepth](imagick.setimagechanneldepth.html) — Встановлює глибину певного каналу зображення
-   [Imagick::setImageClipMask](imagick.setimageclipmask.html) - Встановлює маску кліпу
-   [Imagick::setImageColormapColor](imagick.setimagecolormapcolor.html) — Встановлює колір вказаного індексу картки
-   [Imagick::setImageColorspace](imagick.setimagecolorspace.html) — Встановлює колірний простір зображення
-   [Imagick::setImageCompose](imagick.setimagecompose.html) — Встановлює оператор складеного зображення
-   [Imagick::setImageCompression](imagick.setimagecompression.html) — Встановлює стиснення зображення
-   [Imagick::setImageCompressionQuality](imagick.setimagecompressionquality.html) — Встановлює якість стиснення зображення
-   [Imagick::setImageDelay](imagick.setimagedelay.html) — Встановлює затримку зображення
-   [Imagick::setImageDepth](imagick.setimagedepth.html) — Встановлює глибину зображення
-   [Imagick::setImageDispose](imagick.setimagedispose.html) — Встановлює метод видалення зображення
-   [Imagick::setImageExtent](imagick.setimageextent.html) — Встановлює розмір зображення
-   [Imagick::setImageFilename](imagick.setimagefilename.html) — Встановлює ім'я конкретного файлу.
-   [Imagick::setImageFormat](imagick.setimageformat.html) — Встановлює формат певного зображення
-   [Imagick::setImageGamma](imagick.setimagegamma.html) — Встановлює гаму зображення
-   [Imagick::setImageGravity](imagick.setimagegravity.html) — Встановлює гравітацію зображення
-   [Imagick::setImageGreenPrimary](imagick.setimagegreenprimary.html) — Встановлює кольоровість зображення зеленою первинною точкою.
-   [Imagick::setImageIndex](imagick.setimageindex.html) - Встановлює позицію ітератора
-   [Imagick::setImageInterlaceScheme](imagick.setimageinterlacescheme.html) — Встановлює стиснення зображення
-   [Imagick::setImageInterpolateMethod](imagick.setimageinterpolatemethod.html) — Встановлює метод інтерполяції пікселів зображення
-   [Imagick::setImageIterations](imagick.setimageiterations.html) — Встановлює ітерацію зображення
-   [Imagick::setImageMatte](imagick.setimagematte.html) — Встановлює матовий канал зображення
-   [Imagick::setImageMatteColor](imagick.setimagemattecolor.html) — Встановлює матовий колір зображення
-   [Imagick::setImageOpacity](imagick.setimageopacity.html) — Встановлює рівень непрозорості зображення
-   [Imagick::setImageOrientation](imagick.setimageorientation.html) — Встановлює орієнтацію зображення
-   [Imagick::setImagePage](imagick.setimagepage.html) — Встановлює геометрію сторінки зображення
-   [Imagick::setImageProfile](imagick.setimageprofile.html) - Додає іменований профіль до об'єкту Imagick
-   [Imagick::setImageProperty](imagick.setimageproperty.html) — Встановлює властивість зображення
-   [Imagick::setImageRedPrimary](imagick.setimageredprimary.html) — Встановлює червону первинну точку кольоровості зображення
-   [Imagick::setImageRenderingIntent](imagick.setimagerenderingintent.html) — Встановлює схему передачі кольору зображення
-   [Imagick::setImageResolution](imagick.setimageresolution.html) — Встановлює роздільну здатність зображення
-   [Imagick::setImageScene](imagick.setimagescene.html) — Встановлює сцену зображення
-   [Imagick::setImageTicksPerSecond](imagick.setimagetickspersecond.html) — Встановлює тривалість відображення кадру
-   [Imagick::setImageType](imagick.setimagetype.html) — Встановлює тип зображення
-   [Imagick::setImageUnits](imagick.setimageunits.html) — Встановлює одиниці вимірювання роздільної здатності зображення
-   [Imagick::setImageVirtualPixelMethod](imagick.setimagevirtualpixelmethod.html) - Встановлює метод віртуального пікселя
-   [Imagick::setImageWhitePoint](imagick.setimagewhitepoint.html) — Встановлює білу точку кольору зображення
-   [Imagick::setInterlaceScheme](imagick.setinterlacescheme.html) — Встановлює стиснення зображення
-   [Imagick::setIteratorIndex](imagick.setiteratorindex.html) - Встановлює позицію ітератора
-   [Imagick::setLastIterator](imagick.setlastiterator.html) - Встановлює ітератор Imagick до останнього зображення
-   [Imagick::setOption](imagick.setoption.html) - Встановлює опцію
-   [Imagick::setPage](imagick.setpage.html) — Встановлює геометрію сторінки об'єкту Imagick
-   [Imagick::setPointSize](imagick.setpointsize.html) - Встановлює розмір точки
-   [Imagick::setProgressMonitor](imagick.setprogressmonitor.html) — Встановлює callback-функцію, яка буде викликатись під час обробки зображення Imagick
-   [Imagick::setRegistry](imagick.setregistry.html) - Опис
-   [Imagick::setResolution](imagick.setresolution.html) — Встановлює роздільну здатність зображення
-   [Imagick::setResourceLimit](imagick.setresourcelimit.html) - Встановлює ліміт для конкретного ресурсу
-   [Imagick::setSamplingFactors](imagick.setsamplingfactors.html) — Встановлює коефіцієнти вибірки зображень
-   [Imagick::setSize](imagick.setsize.html) — Встановлює розмір об'єкту Imagick
-   [Imagick::setSizeOffset](imagick.setsizeoffset.html) — Встановлює розмір та усунення об'єкта Imagick
-   [Imagick::setType](imagick.settype.html) — Встановлює атрибут типу зображення
-   [Imagick::shadeImage](imagick.shadeimage.html) — Створює 3D-ефект
-   [Imagick::shadowImage](imagick.shadowimage.html) — Імітує тінь зображення
-   [Imagick::sharpenImage](imagick.sharpenimage.html) — Підвищує різкість зображення
-   [Imagick::shaveImage](imagick.shaveimage.html) — Видаляє пікселі по краях зображення
-   [Imagick::shearImage](imagick.shearimage.html) - Створює паралелограм
-   [Imagick::sigmoidalContrastImage](imagick.sigmoidalcontrastimage.html) - Регулює контраст зображення
-   [Imagick::sketchImage](imagick.sketchimage.html) - Імітує малюнок олівцем
-   [Imagick::smushImages](imagick.smushimages.html) - Опис
-   [Imagick::solarizeImage](imagick.solarizeimage.html) — Застосовує до зображення ефект соляризації
-   [Imagick::sparseColorImage](imagick.sparsecolorimage.html) - Інтерполює кольори
-   [Imagick::spliceImage](imagick.spliceimage.html) — Склеює суцільний колір у зображення
-   [Imagick::spreadImage](imagick.spreadimage.html) — Випадково зміщує кожен піксель у блоці
-   [Imagick::statisticImage](imagick.statisticimage.html) - Опис
-   [Imagick::steganoImage](imagick.steganoimage.html) — Приховує цифровий водяний знак у зображенні
-   [Imagick::stereoImage](imagick.stereoimage.html) — Об'єднує два зображення
-   [Imagick::stripImage](imagick.stripimage.html) — Знімає зображення всіх профілів та коментарів
-   [Imagick::subImageMatch](imagick.subimagematch.html) - Опис
-   [Imagick::swirlImage](imagick.swirlimage.html) — Закручує пікселі навколо центру зображення
-   [Imagick::textureImage](imagick.textureimage.html) — Багато разів розміщує зображення текстури
-   [Imagick::thresholdImage](imagick.thresholdimage.html) - Змінює окремі пікселі на основі порогового значення
-   [Imagick::thumbnailImage](imagick.thumbnailimage.html) — Змінює розмір зображення
-   [Imagick::tintImage](imagick.tintimage.html) — Застосовує вектор кольору до кожного пікселя зображення
-   [Imagick::toString](imagick.tostring.html) — Повертає зображення у вигляді рядка
-   [Imagick::transformImage](imagick.transformimage.html) — Зручний метод налаштування розміру кадрування та геометрії зображення
-   [Imagick::transformImageColorspace](imagick.transformimagecolorspace.html) — Перетворює зображення на новий колірний простір
-   [Imagick::transparentPaintImage](imagick.transparentpaintimage.html) — Малює пікселі прозорими
-   [Imagick::transposeImage](imagick.transposeimage.html) — Створює вертикальне дзеркальне відображення
-   [Imagick::transverseImage](imagick.transverseimage.html) — Створює горизонтальне дзеркальне відображення
-   [Imagick::trimImage](imagick.trimimage.html) — Видаляє краї із зображення
-   [Imagick::uniqueImageColors](imagick.uniqueimagecolors.html) - Відкидає все, крім одного, будь-якого кольору пікселя
-   [Imagick::unsharpMaskImage](imagick.unsharpmaskimage.html) - Різкість зображення
-   [Imagick::valid](imagick.valid.html) — Перевіряє, чи поточний елемент є коректним.
-   [Imagick::vignetteImage](imagick.vignetteimage.html) — Додає він'єтний фільтр до зображення
-   [Imagick::waveImage](imagick.waveimage.html) — Застосовує хвильовий фільтр до зображення
-   [Imagick::whiteThresholdImage](imagick.whitethresholdimage.html) — Зафарбовує всі пікселі вище за поріг у білий
-   [Imagick::writeImage](imagick.writeimage.html) — Записує зображення за вказаним ім'ям файлу
-   [Imagick::writeImageFile](imagick.writeimagefile.html) — Записує зображення у файл
-   [Imagick::writeImages](imagick.writeimages.html) — Записує зображення або послідовність зображень
-   [Imagick::writeImagesFile](imagick.writeimagesfile.html) — Записує кадри у файловий дескриптор