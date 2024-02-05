---
navigation:
  - imagick.examples-1.md: « Базове використання
  - imagick.adaptiveblurimage.md: 'Imagick::adaptiveBlurImage »'
  - index.md: PHP Manual
  - book.imagick.md: ImageMagick
title: 'Класс[Imagick](class.imagick.md)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Класс[Imagick](class.imagick.md)

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
public profileImage(string $name, ?string $profile): bool
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
public scaleImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
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
public setImageBiasQuantum(float $bias): void
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

| Эффекты изображения | Методы получения | Методы установки | Чтение/запись изображений | Другие |
| --- | --- | --- | --- | --- |
| [Imagick::adaptiveBlurImage()](imagick.adaptiveblurimage.md) | [Imagick::getCompression()](imagick.getcompression.md) | [Imagick::setBackgroundColor()](imagick.setbackgroundcolor.md) | [Imagick::\_\_construct()](imagick.construct.md) | [Imagick::clear()](imagick.clear.md) |
| [Imagick::adaptiveResizeImage()](imagick.adaptiveresizeimage.md) | [Imagick::getFilename()](imagick.getfilename.md) | [Imagick::setCompressionQuality()](imagick.setcompressionquality.md) | [Imagick::addImage()](imagick.addimage.md) | [Imagick::clone()](imagick.clone.md) |
| [Imagick::adaptiveSharpenImage()](imagick.adaptivesharpenimage.md) | [Imagick::getFormat()](imagick.getformat.md) | [Imagick::setCompression()](imagick.setcompression.md) | [Imagick::appendImages()](imagick.appendimages.md) | [Imagick::current()](imagick.current.md) |
| [Imagick::adaptiveThresholdImage()](imagick.adaptivethresholdimage.md) | [Imagick::getImageBackgroundColor()](imagick.getimagebackgroundcolor.md) | [Imagick::setFilename()](imagick.setfilename.md) | [Imagick::getFilename()](imagick.getfilename.md) | [Imagick::destroy()](imagick.destroy.md) |
| [Imagick::addNoiseImage()](imagick.addnoiseimage.md) | [Imagick::getImageBlob()](imagick.getimageblob.md) | [Imagick::getImagesBlob()](imagick.getimagesblob.md) | [Imagick::setFormat()](imagick.setformat.md) | [Imagick::getFormat()](imagick.getformat.md) |
| [Imagick::affinetransformimage()](imagick.affinetransformimage.md) | [Imagick::getImageBluePrimary()](imagick.getimageblueprimary.md) | [Imagick::setImageBackgroundColor()](imagick.setimagebackgroundcolor.md) | [Imagick::getImageFilename()](imagick.getimagefilename.md) | [Imagick::getHomeURL()](imagick.gethomeurl.md) |
| [Imagick::annotateImage()](imagick.annotateimage.md) | [Imagick::getImageBorderColor()](imagick.getimagebordercolor.md) | [Imagick::setFirstIterator()](imagick.setfirstiterator.md) | [Imagick::getImageFormat()](imagick.getimageformat.md) | [Imagick::commentImage()](imagick.commentimage.md) |
| [Imagick::averageImages()](imagick.averageimages.md) | [Imagick::getImageChannelDepth()](imagick.getimagechanneldepth.md) | [Imagick::setImageBias()](imagick.setimagebias.md) | [Imagick::getImage()](imagick.getimage.md) | [Imagick::getNumberImages()](imagick.getnumberimages.md) |
| [Imagick::blackThresholdImage()](imagick.blackthresholdimage.md) | [Imagick::getImageChannelDistortion()](imagick.getimagechanneldistortion.md) | [Imagick::setImageBluePrimary()](imagick.setimageblueprimary.md) | [Imagick::setImageFilename()](imagick.setimagefilename.md) | [Imagick::getReleaseDate()](imagick.getreleasedate.md) |
| [Imagick::blurImage()](imagick.blurimage.md) | [Imagick::getImageChannelExtrema()](imagick.getimagechannelextrema.md) | [Imagick::setImageBorderColor()](imagick.setimagebordercolor.md) | [Imagick::setImageFormat()](imagick.setimageformat.md) | [Imagick::getVersion()](imagick.getversion.md) |
| [Imagick::borderImage()](imagick.borderimage.md) | [Imagick::getImageChannelMean()](imagick.getimagechannelmean.md) | [Imagick::setImageChannelDepth()](imagick.setimagechanneldepth.md) | [Imagick::readImageFile()](imagick.readimagefile.md) | [Imagick::hasNextImage()](imagick.hasnextimage.md) |
| [Imagick::charcoalImage()](imagick.charcoalimage.md) | [Imagick::getImageChannelStatistics()](imagick.getimagechannelstatistics.md) | [Imagick::setImageColormapColor()](imagick.setimagecolormapcolor.md) | [Imagick::readImage()](imagick.readimage.md) | [Imagick::hasPreviousImage()](imagick.haspreviousimage.md) |
| [Imagick::chopImage()](imagick.chopimage.md) | [Imagick::getImageColormapColor()](imagick.getimagecolormapcolor.md) | [Imagick::setImageColorSpace()](imagick.setimagecolorspace.md) | [Imagick::writeImages()](imagick.writeimages.md) | [Imagick::labelImage()](imagick.labelimage.md) |
| [Imagick::clipImage()](imagick.clipimage.md) | [Imagick::getImageColorspace()](imagick.getimagecolorspace.md) | [Imagick::setImageCompose()](imagick.setimagecompose.md) | [Imagick::writeImage()](imagick.writeimage.md) | [Imagick::newImage()](imagick.newimage.md) |
| [Imagick::clipPathImage()](imagick.clippathimage.md) | [Imagick::getImageColors()](imagick.getimagecolors.md) | [Imagick::setImageCompression()](imagick.setimagecompression.md) |  | [Imagick::newPseudoImage()](imagick.newpseudoimage.md) |
| [Imagick::coalesceImages()](imagick.coalesceimages.md) | [Imagick::getImageCompose()](imagick.getimagecompose.md) | [Imagick::setImageDelay()](imagick.setimagedelay.md) |  | [Imagick::nextImage()](imagick.nextimage.md) |
| [Imagick::colorFloodFillImage()](imagick.colorfloodfillimage.md) | [Imagick::getImageDelay()](imagick.getimagedelay.md) | [Imagick::setImageDepth()](imagick.setimagedepth.md) |  | [Imagick::pingImageBlob()](imagick.pingimageblob.md) |
| [Imagick::colorizeImage()](imagick.colorizeimage.md) | [Imagick::getImageDepth()](imagick.getimagedepth.md) | [Imagick::setImageDispose()](imagick.setimagedispose.md) |  | [Imagick::pingImageFile()](imagick.pingimagefile.md) |
| [Imagick::combineImages()](imagick.combineimages.md) | [Imagick::getImageDispose()](imagick.getimagedispose.md) | [Imagick::setImageDispose()](imagick.setimagedispose.md) |  | [Imagick::pingImage()](imagick.pingimage.md) |
| [Imagick::compareImageChannels()](imagick.compareimagechannels.md) | [Imagick::getImageDistortion()](imagick.getimagedistortion.md) | [Imagick::setImageExtent()](imagick.setimageextent.md) |  | [Imagick::previousImage()](imagick.previousimage.md) |
| [Imagick::compareImageLayers()](imagick.compareimagelayers.md) | [Imagick::getImageExtrema()](imagick.getimageextrema.md) | [Imagick::setImageFilename()](imagick.setimagefilename.md) |  | [Imagick::profileImage()](imagick.profileimage.md) |
| [Imagick::compositeImage()](imagick.compositeimage.md) | [Imagick::getImageFilename()](imagick.getimagefilename.md) | [Imagick::setImageFormat()](imagick.setimageformat.md) |  | [Imagick::queryFormats()](imagick.queryformats.md) |
| [Imagick::contrastImage()](imagick.contrastimage.md) | [Imagick::getImageFormat()](imagick.getimageformat.md) | [Imagick::setImageGamma()](imagick.setimagegamma.md) |  | [Imagick::removeImageProfile()](imagick.removeimageprofile.md) |
| [Imagick::contrastStretchImage()](imagick.contraststretchimage.md) | [Imagick::getImageGamma()](imagick.getimagegamma.md) | [Imagick::setImageGreenPrimary()](imagick.setimagegreenprimary.md) |  | [Imagick::removeImage()](imagick.removeimage.md) |
| [Imagick::convolveImage()](imagick.convolveimage.md) | [Imagick::getImageGeometry()](imagick.getimagegeometry.md) | [Imagick::setImageIndex()](imagick.setimageindex.md) |  | [Imagick::setFirstIterator()](imagick.setfirstiterator.md) |
| [Imagick::cropImage()](imagick.cropimage.md) | [Imagick::getImageGreenPrimary()](imagick.getimagegreenprimary.md) | [Imagick::setImageInterpolateMethod()](imagick.setimageinterpolatemethod.md) |  | [Imagick::setImageIndex()](imagick.setimageindex.md) |
| [Imagick::cycleColormapImage()](imagick.cyclecolormapimage.md) | [Imagick::getImageHeight()](imagick.getimageheight.md) | [Imagick::setImageIterations()](imagick.setimageiterations.md) |  | [Imagick::valid()](imagick.valid.md) |
| [Imagick::deconstructImages()](imagick.deconstructimages.md) | [Imagick::getImageHistogram()](imagick.getimagehistogram.md) | [Imagick::setImageMatteColor()](imagick.setimagemattecolor.md) |  | [Imagick::getCopyright()](imagick.getcopyright.md) |
| [Imagick::drawImage()](imagick.drawimage.md) | [Imagick::getImageIndex()](imagick.getimageindex.md) | [Imagick::setImageMatte()](imagick.setimagematte.md) |  |  |
| [Imagick::edgeImage()](imagick.edgeimage.md) | [Imagick::getImageInterlaceScheme()](imagick.getimageinterlacescheme.md) | [Imagick::setImagePage()](imagick.setimagepage.md) |  |  |
| [Imagick::embossImage()](imagick.embossimage.md) | [Imagick::getImageInterpolateMethod()](imagick.getimageinterpolatemethod.md) | [Imagick::setImageProfile()](imagick.setimageprofile.md) |  |  |
| [Imagick::enhanceImage()](imagick.enhanceimage.md) | [Imagick::getImageIterations()](imagick.getimageiterations.md) | [Imagick::setImageProperty()](imagick.setimageproperty.md) |  |  |
| [Imagick::equalizeImage()](imagick.equalizeimage.md) | [Imagick::getImageMatteColor()](imagick.getimagemattecolor.md) | [Imagick::setImageRedPrimary()](imagick.setimageredprimary.md) |  |  |
| [Imagick::evaluateImage()](imagick.evaluateimage.md) | [Imagick::getImageMatte()](imagick.getimagematte.md) | [Imagick::setImageRenderingIntent()](imagick.setimagerenderingintent.md) |  |  |
| [Imagick::flattenImages()](imagick.flattenimages.md) | [Imagick::getImagePage()](imagick.getimagepage.md) | [Imagick::setImageResolution()](imagick.setimageresolution.md) |  |  |
| [Imagick::flipImage()](imagick.flipimage.md) | [Imagick::getImagePixelColor()](imagick.getimagepixelcolor.md) | [Imagick::setImageScene()](imagick.setimagescene.md) |  |  |
| [Imagick::flopImage()](imagick.flopimage.md) | [Imagick::getImageProfile()](imagick.getimageprofile.md) | [Imagick::setImageTicksPerSecond()](imagick.setimagetickspersecond.md) |  |  |
|  | [Imagick::getImageProperty()](imagick.getimageproperty.md) | [Imagick::setImageType()](imagick.setimagetype.md) |  |  |
| [Imagick::fxImage()](imagick.fximage.md) | [Imagick::getImageRedPrimary()](imagick.getimageredprimary.md) | [Imagick::setImageUnits()](imagick.setimageunits.md) |  |  |
| [Imagick::gammaImage()](imagick.gammaimage.md) | [Imagick::getImageRegion()](imagick.getimageregion.md) | [Imagick::setImageVirtualPixelMethod()](imagick.setimagevirtualpixelmethod.md) |  |  |
| [Imagick::gaussianBlurImage()](imagick.gaussianblurimage.md) | [Imagick::getImageRenderingIntent()](imagick.getimagerenderingintent.md) | [Imagick::setImageWhitepoint()](imagick.setimagewhitepoint.md) |  |  |
| [Imagick::implodeImage()](imagick.implodeimage.md) | [Imagick::getImageResolution()](imagick.getimageresolution.md) | [Imagick::setInterlaceScheme()](imagick.setinterlacescheme.md) |  |  |
| [Imagick::levelImage()](imagick.levelimage.md) | [Imagick::getImageScene()](imagick.getimagescene.md) | [Imagick::setOption()](imagick.setoption.md) |  |  |
| [Imagick::linearStretchImage()](imagick.linearstretchimage.md) | [Imagick::getImageSignature()](imagick.getimagesignature.md) | [Imagick::setPage()](imagick.setpage.md) |  |  |
| [Imagick::magnifyImage()](imagick.magnifyimage.md) | [Imagick::getImageTicksPerSecond()](imagick.getimagetickspersecond.md) | [Imagick::setResolution()](imagick.setresolution.md) |  |  |
| [Imagick::matteFloodFillImage()](imagick.mattefloodfillimage.md) | [Imagick::getImageTotalInkDensity()](imagick.getimagetotalinkdensity.md) | [Imagick::setResourceLimit()](imagick.setresourcelimit.md) |  |  |
| [Imagick::medianFilterImage()](imagick.medianfilterimage.md) | [Imagick::getImageType()](imagick.getimagetype.md) | [Imagick::setSamplingFactors()](imagick.setsamplingfactors.md) |  |  |
| [Imagick::minifyImage()](imagick.minifyimage.md) | [Imagick::getImageUnits()](imagick.getimageunits.md) | [Imagick::setSizeOffset()](imagick.setsizeoffset.md) |  |  |
| [Imagick::modulateImage()](imagick.modulateimage.md) | [Imagick::getImageVirtualPixelMethod()](imagick.getimagevirtualpixelmethod.md) | [Imagick::setSize()](imagick.setsize.md) |  |  |
| [Imagick::montageImage()](imagick.montageimage.md) | [Imagick::getImageWhitepoint()](imagick.getimagewhitepoint.md) | [Imagick::setType()](imagick.settype.md) |  |  |
| [Imagick::morphImages()](imagick.morphimages.md) | [Imagick::getImageWidth()](imagick.getimagewidth.md) |  |  |  |
| [Imagick::mosaicImages()](imagick.mosaicimages.md) | [Imagick::getImage()](imagick.getimage.md) |  |  |  |
| [Imagick::motionBlurImage()](imagick.motionblurimage.md) | [Imagick::getInterlaceScheme()](imagick.getinterlacescheme.md) |  |  |  |
| [Imagick::negateImage()](imagick.negateimage.md) | [Imagick::getNumberImages()](imagick.getnumberimages.md) |  |  |  |
| [Imagick::normalizeImage()](imagick.normalizeimage.md) | [Imagick::getOption()](imagick.getoption.md) |  |  |  |
| [Imagick::oilPaintImage()](imagick.oilpaintimage.md) | [Imagick::getPackageName()](imagick.getpackagename.md) |  |  |  |
| [Imagick::optimizeImageLayers()](imagick.optimizeimagelayers.md) | [Imagick::getPage()](imagick.getpage.md) |  |  |  |
| [Imagick::paintOpaqueImage()](imagick.paintopaqueimage.md) | [Imagick::getPixelIterator()](imagick.getpixeliterator.md) |  |  |  |
| [Imagick::paintTransparentImage()](imagick.painttransparentimage.md) | [Imagick::getPixelRegionIterator()](imagick.getpixelregioniterator.md) |  |  |  |
| [Imagick::posterizeImage()](imagick.posterizeimage.md) | [Imagick::getQuantumDepth()](imagick.getquantumdepth.md) |  |  |  |
| [Imagick::radialBlurImage()](imagick.radialblurimage.md) | [Imagick::getQuantumRange()](imagick.getquantumrange.md) |  |  |  |
| [Imagick::raiseImage()](imagick.raiseimage.md) | [Imagick::getResourceLimit()](imagick.getresourcelimit.md) |  |  |  |
| [Imagick::randomThresholdImage()](imagick.randomthresholdimage.md) | [Imagick::getResource()](imagick.getresource.md) |  |  |  |
| [Imagick::reduceNoiseImage()](imagick.reducenoiseimage.md) | [Imagick::getSamplingFactors()](imagick.getsamplingfactors.md) |  |  |  |
| [Imagick::render()](imagick.render.md) | [Imagick::getSizeOffset()](imagick.getsizeoffset.md) |  |  |  |
| [Imagick::resampleImage()](imagick.resampleimage.md) | [Imagick::getSize()](imagick.getsize.md) |  |  |  |
| [Imagick::resizeImage()](imagick.resizeimage.md) | [Imagick::identifyImage()](imagick.identifyimage.md) |  |  |  |
| [Imagick::rollImage()](imagick.rollimage.md) | [Imagick::getImageSize()](imagick.getimagesize.md) |  |  |  |
| [Imagick::rotateImage()](imagick.rotateimage.md) |  |  |  |  |
| [Imagick::sampleImage()](imagick.sampleimage.md) |  |  |  |  |
| [Imagick::scaleImage()](imagick.scaleimage.md) |  |  |  |  |
| [Imagick::separateImageChannel()](imagick.separateimagechannel.md) |  |  |  |  |
| [Imagick::sepiaToneImage()](imagick.sepiatoneimage.md) |  |  |  |  |
| [Imagick::shadeImage()](imagick.shadeimage.md) |  |  |  |  |
| [Imagick::shadowImage()](imagick.shadowimage.md) |  |  |  |  |
| [Imagick::sharpenImage()](imagick.sharpenimage.md) |  |  |  |  |
| [Imagick::shaveImage()](imagick.shaveimage.md) |  |  |  |  |
| [Imagick::shearImage()](imagick.shearimage.md) |  |  |  |  |
| [Imagick::sigmoidalContrastImage()](imagick.sigmoidalcontrastimage.md) |  |  |  |  |
| [Imagick::sketchImage()](imagick.sketchimage.md) |  |  |  |  |
| [Imagick::solarizeImage()](imagick.solarizeimage.md) |  |  |  |  |
| [Imagick::spliceImage()](imagick.spliceimage.md) |  |  |  |  |
| [Imagick::spreadImage()](imagick.spreadimage.md) |  |  |  |  |
| [Imagick::steganoImage()](imagick.steganoimage.md) |  |  |  |  |
| [Imagick::stereoImage()](imagick.stereoimage.md) |  |  |  |  |
| [Imagick::stripImage()](imagick.stripimage.md) |  |  |  |  |
| [Imagick::swirlImage()](imagick.swirlimage.md) |  |  |  |  |
| [Imagick::textureImage()](imagick.textureimage.md) |  |  |  |  |
| [Imagick::thresholdImage()](imagick.thresholdimage.md) |  |  |  |  |
| [Imagick::thumbnailImage()](imagick.thumbnailimage.md) |  |  |  |  |
| [Imagick::tintImage()](imagick.tintimage.md) |  |  |  |  |
| [Imagick::transverseImage()](imagick.transverseimage.md) |  |  |  |  |
| [Imagick::trimImage()](imagick.trimimage.md) |  |  |  |  |
| [Imagick::uniqueImageColors()](imagick.uniqueimagecolors.md) |  |  |  |  |
| [Imagick::unsharpMaskImage()](imagick.unsharpmaskimage.md) |  |  |  |  |
| [Imagick::vignetteImage()](imagick.vignetteimage.md) |  |  |  |  |
| [Imagick::waveImage()](imagick.waveimage.md) |  |  |  |  |
| [Imagick::whiteThresholdImage()](imagick.whitethresholdimage.md) |  |  |  |  |

## Зміст

-   [Imagick::adaptiveBlurImage](imagick.adaptiveblurimage.md)— Додає адаптивний фільтр розмиття до зображення
-   [Imagick::adaptiveResizeImage](imagick.adaptiveresizeimage.md)— Адаптивна зміна розміру зображення з даними тріангуляції
-   [Imagick::adaptiveSharpenImage](imagick.adaptivesharpenimage.md)— Адаптивна зміна різкості зображення
-   [Imagick::adaptiveThresholdImage](imagick.adaptivethresholdimage.md)— Вибір порога кожного пікселя в залежності від діапазону інтенсивності
-   [Imagick::addImage](imagick.addimage.md)— Додає нове зображення до списку зображень об'єкту Imagick
-   [Imagick::addNoiseImage](imagick.addnoiseimage.md) \- Накладає випадковий шум на зображення
-   [Imagick::affineTransformImage](imagick.affinetransformimage.md)— Перетворює зображення
-   [Imagick::animateImages](imagick.animateimages.md)— Анімація одного або кількох зображень
-   [Imagick::annotateImage](imagick.annotateimage.md)— Додає текстовий коментар на зображення
-   [Imagick::appendImages](imagick.appendimages.md)— Об'єднує набір зображень
-   [Imagick::autoLevelImage](imagick.autolevelimage.md)— Налаштовує рівні певного каналу зображення
-   [Imagick::averageImages](imagick.averageimages.md)— Усереднює набір зображень
-   [Imagick::blackThresholdImage](imagick.blackthresholdimage.md)— Перевести всі пікселі нижче граничного значення в чорний колір
-   [Imagick::blueShiftImage](imagick.blueshiftimage.md)— Приглушує кольори зображення
-   [Imagick::blurImage](imagick.blurimage.md)— Додає фільтр розмиття до зображення
-   [Imagick::borderImage](imagick.borderimage.md)— Оточує зображення рамкою
-   [Imagick::brightnessContrastImage](imagick.brightnesscontrastimage.md)— Змінює яскравість та/або контраст зображення
-   [Imagick::charcoalImage](imagick.charcoalimage.md) \- Малювання вугіллям
-   [Imagick::chopImage](imagick.chopimage.md)— Видаляє область зображення та обрізає його.
-   [Imagick::clampImage](imagick.clampimage.md) \- Обмежує діапазон кольорів від 0 до квантової глибини.
-   [Imagick::clear](imagick.clear.md)— Очищає всі ресурси, пов'язані з об'єктом Imagick
-   [Imagick::clipImage](imagick.clipimage.md)— Обрізка вздовж найближчого контуру з профілем 8BIM
-   [Imagick::clipImagePath](imagick.clipimagepath.md)— Кліпи вздовж іменованих шляхів із профілю 8BIM, якщо вони є
-   [Imagick::clipPathImage](imagick.clippathimage.md)— Відсікти уздовж зазначеного контуру з профілем 8BIM
-   [Imagick::clone](imagick.clone.md)— Створює точну копію об'єкту Imagick
-   [Imagick::clutImage](imagick.clutimage.md)— Замінює кольори у зображенні
-   [Imagick::coalesceImages](imagick.coalesceimages.md)— Компонує набір зображень
-   [Imagick::colorFloodfillImage](imagick.colorfloodfillimage.md)— Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::colorizeImage](imagick.colorizeimage.md)— Змішування кольору заливки із зображенням
-   [Imagick::colorMatrixImage](imagick.colormatriximage.md)— Застосовує перетворення кольору до зображення
-   [Imagick::combineImages](imagick.combineimages.md)— Об'єднує одне або кілька зображень в одне зображення
-   [Imagick::commentImage](imagick.commentimage.md)— Додає коментар до вашого зображення
-   [Imagick::compareImageChannels](imagick.compareimagechannels.md)— Повертає різницю в одному чи кількох зображеннях
-   [Imagick::compareImageLayers](imagick.compareimagelayers.md)— Повертає максимальну область, що обмежує між зображеннями.
-   [Imagick::compareImages](imagick.compareimages.md)— Порівнює зображення з відновленим зображенням
-   [Imagick::compositeImage](imagick.compositeimage.md)— Накладає одне зображення на інше
-   [Imagick::\_\_construct](imagick.construct.md) \- Конструктор об'єкту Imagick
-   [Imagick::contrastImage](imagick.contrastimage.md)— Змінює контраст зображення
-   [Imagick::contrastStretchImage](imagick.contraststretchimage.md)— Підвищує контрастність кольорового зображення
-   [Imagick::convolveImage](imagick.convolveimage.md)— Застосовується ядро ​​згортки для користувача.
-   [Imagick::count](imagick.count.md)— Отримує кількість зображень
-   [Imagick::cropImage](imagick.cropimage.md)— Витягує область зображення
-   [Imagick::cropThumbnailImage](imagick.cropthumbnailimage.md) \- Створює обрізану мініатюру
-   [Imagick::current](imagick.current.md)— Повертає посилання на поточний об'єкт Imagick
-   [Imagick::cycleColormapImage](imagick.cyclecolormapimage.md)— Відображає карту кольорів зображення
-   [Imagick::decipherImage](imagick.decipherimage.md)— Розшифровує зображення
-   [Imagick::deconstructImages](imagick.deconstructimages.md)— Повертає певні піксельні відмінності між зображеннями
-   [Imagick::deleteImageArtifact](imagick.deleteimageartifact.md)— Видаляє артефакт зображення
-   [Imagick::deleteImageProperty](imagick.deleteimageproperty.md)— Видаляє властивість зображення
-   [Imagick::deskewImage](imagick.deskewimage.md)— Видаляє перекіс із зображення
-   [Imagick::despeckleImage](imagick.despeckleimage.md) \- Зменшує спекл-шум на зображенні
-   [Imagick::destroy](imagick.destroy.md)— Видаляє об'єкт Imagick
-   [Imagick::displayImage](imagick.displayimage.md)— Виводить зображення
-   [Imagick::displayImages](imagick.displayimages.md)— Виводить зображення або послідовність зображень
-   [Imagick::distortImage](imagick.distortimage.md)— Спотворює зображення, використовуючи різні методи спотворення
-   [Imagick::drawImage](imagick.drawimage.md)— Виконує рендеринг об'єкту ImagickDraw на поточному зображенні
-   [Imagick::edgeImage](imagick.edgeimage.md)— Підсилює краї зображення.
-   [Imagick::embossImage](imagick.embossimage.md)— Повертає зображення у градаціях сірого із тривимірним ефектом
-   [Imagick::encipherImage](imagick.encipherimage.md) \- Шифрує зображення
-   [Imagick::enhanceImage](imagick.enhanceimage.md)— Покращує якість шумного зображення
-   [Imagick::equalizeImage](imagick.equalizeimage.md)— Вирівнює гістограму зображення
-   [Imagick::evaluateImage](imagick.evaluateimage.md)— Застосовує вираз до зображення
-   [Imagick::exportImagePixels](imagick.exportimagepixels.md)— Експортує пікселі зображення
-   [Imagick::extentImage](imagick.extentimage.md)— Встановлює розмір зображення
-   [Imagick::filter](imagick.filter.md)— Застосовується ядро ​​згортки для користувача.
-   [Imagick::flattenImages](imagick.flattenimages.md)— Поєднує послідовність зображень
-   [Imagick::flipImage](imagick.flipimage.md)— Створює вертикальне дзеркало зображення
-   [Imagick::floodFillPaintImage](imagick.floodfillpaintimage.md)— Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::flopImage](imagick.flopimage.md)— Створює горизонтальне дзеркальне відображення
-   [Imagick::forwardFourierTransformImage](imagick.forwardfouriertransformimage.md) \- Реалізує дискретне перетворення Фур'є
-   [Imagick::frameImage](imagick.frameimage.md)— Додає імітацію тривимірного кордону
-   [Imagick::functionImage](imagick.functionimage.md)— Застосовує функцію зображення.
-   [Imagick::fxImage](imagick.fximage.md)— Оцінює вираз для кожного пікселя у зображенні
-   [Imagick::gammaImage](imagick.gammaimage.md) \- Гамма-корекція зображення
-   [Imagick::gaussianBlurImage](imagick.gaussianblurimage.md)— Розмиває зображення
-   [Imagick::getColorspace](imagick.getcolorspace.md)— Повертає палітру кольорів
-   [Imagick::getCompression](imagick.getcompression.md)— Повертає тип стиснення об'єкта
-   [Imagick::getCompressionQuality](imagick.getcompressionquality.md)— Повертає якість стиснення об'єкта
-   [Imagick::getCopyright](imagick.getcopyright.md)— Повертає копірайт API ImageMagick у вигляді рядка
-   [Imagick::getFilename](imagick.getfilename.md) \- Ім'я файлу результуючого зображення
-   [Imagick::getFont](imagick.getfont.md)— Повертає назву шрифту
-   [Imagick::getFormat](imagick.getformat.md)— Повертає формат Imagick об'єкту
-   [Imagick::getGravity](imagick.getgravity.md) \- Повертає значення гравітації (тяжіння)
-   [Imagick::getHomeURL](imagick.gethomeurl.md)— Повертає домашню URL-адресу бібліотеки ImageMagick
-   [Imagick::getImage](imagick.getimage.md)— Повертає новий об'єкт Imagick
-   [Imagick::getImageAlphaChannel](imagick.getimagealphachannel.md)— Перевіряє, чи є зображення альфа-канал
-   [Imagick::getImageArtifact](imagick.getimageartifact.md)— Повертає артефакт зображення
-   [Imagick::getImageAttribute](imagick.getimageattribute.md) \- Повертає іменований атрибут
-   [Imagick::getImageBackgroundColor](imagick.getimagebackgroundcolor.md)— Повертає колір тла зображення
-   [Imagick::getImageBlob](imagick.getimageblob.md)— Повертає послідовність зображень у вигляді BLOB
-   [Imagick::getImageBluePrimary](imagick.getimageblueprimary.md)— Повертає основну точку синього кольору зображення
-   [Imagick::getImageBorderColor](imagick.getimagebordercolor.md)— Повертає колір рамки зображення
-   [Imagick::getImageChannelDepth](imagick.getimagechanneldepth.md)— Повертає глибину для певного каналу зображення
-   [Imagick::getImageChannelDistortion](imagick.getimagechanneldistortion.md)— Порівнює канали зображення з відновленим зображенням
-   [Imagick::getImageChannelDistortions](imagick.getimagechanneldistortions.md)— Повертає спотворення каналу
-   [Imagick::getImageChannelExtrema](imagick.getimagechannelextrema.md)— Повертає екстремуми для одного або кількох каналів зображення
-   [Imagick::getImageChannelKurtosis](imagick.getimagechannelkurtosis.md)— Повертає ексцес та асиметрію певного каналу
-   [Imagick::getImageChannelMean](imagick.getimagechannelmean.md)— Повертає середнє та стандартне відхилення
-   [Imagick::getImageChannelRange](imagick.getimagechannelrange.md)— Повертає діапазон каналів
-   [Imagick::getImageChannelStatistics](imagick.getimagechannelstatistics.md)— Повертає статистику для кожного каналу зображення
-   [Imagick::getImageClipMask](imagick.getimageclipmask.md)— Повертає відсічну маску зображення
-   [Imagick::getImageColormapColor](imagick.getimagecolormapcolor.md)— Повертає колір зазначеного індексу палітри
-   [Imagick::getImageColors](imagick.getimagecolors.md)— Повертає кількість унікальних кольорів у зображенні
-   [Imagick::getImageColorspace](imagick.getimagecolorspace.md)— Повертає палітру кольорів зображення
-   [Imagick::getImageCompose](imagick.getimagecompose.md)— Повертає складовий оператор, пов'язаний із зображенням
-   [Imagick::getImageCompression](imagick.getimagecompression.md)— Повертає поточний тип компресії зображення
-   [Imagick::getImageCompressionQuality](imagick.getimagecompressionquality.md)— Повертає поточну якість стиснення зображення
-   [Imagick::getImageDelay](imagick.getimagedelay.md)— Повертає затримку зображення
-   [Imagick::getImageDepth](imagick.getimagedepth.md)— Повертає глибину зображення
-   [Imagick::getImageDispose](imagick.getimagedispose.md)— Повертає метод видалення зображення
-   [Imagick::getImageDistortion](imagick.getimagedistortion.md)— Порівнює зображення з відновленим зображенням
-   [Imagick::getImageExtrema](imagick.getimageextrema.md)— Повертає екстремуми зображення
-   [Imagick::getImageFilename](imagick.getimagefilename.md)— Повертає ім'я файлу конкретного зображення у послідовності
-   [Imagick::getImageFormat](imagick.getimageformat.md)— Повертає формат зображення в послідовності.
-   [Imagick::getImageGamma](imagick.getimagegamma.md)— Повертає гаму зображення
-   [Imagick::getImageGeometry](imagick.getimagegeometry.md)— Повертає ширину та висоту у вигляді асоціативного масиву
-   [Imagick::getImageGravity](imagick.getimagegravity.md) \- Повертає значення гравітації (тяжіння)
-   [Imagick::getImageGreenPrimary](imagick.getimagegreenprimary.md)— Повертає первинну точку кольоровості зеленого
-   [Imagick::getImageHeight](imagick.getimageheight.md)— Повертає висоту зображення
-   [Imagick::getImageHistogram](imagick.getimagehistogram.md)— Повертає гістограму зображення
-   [Imagick::getImageIndex](imagick.getimageindex.md)— Повертає індекс активного поточного зображення.
-   [Imagick::getImageInterlaceScheme](imagick.getimageinterlacescheme.md)— Отримує схему надрядкового зображення
-   [Imagick::getImageInterpolateMethod](imagick.getimageinterpolatemethod.md)— Повертає метод інтерполяції
-   [Imagick::getImageIterations](imagick.getimageiterations.md)— Повертає ітерацію зображення
-   [Imagick::getImageLength](imagick.getimagelength.md)— Повертає довжину зображення у байтах
-   [Imagick::getImageMatte](imagick.getimagematte.md)— Повертає, якщо зображення містить матовий канал
-   [Imagick::getImageMatteColor](imagick.getimagemattecolor.md)— Повертає матовий колір зображення
-   [Imagick::getImageMimeType](imagick.getimagemimetype.md)— Повертає MIME-тип зображення
-   [Imagick::getImageOrientation](imagick.getimageorientation.md)— Повертає орієнтацію зображення
-   [Imagick::getImagePage](imagick.getimagepage.md)— Повертає геометрію сторінки
-   [Imagick::getImagePixelColor](imagick.getimagepixelcolor.md)— Повертає колір вказаного пікселя
-   [Imagick::getImageProfile](imagick.getimageprofile.md)— Повертає іменований профіль зображення
-   [Imagick::getImageProfiles](imagick.getimageprofiles.md)— Повертає профілі зображень
-   [Imagick::getImageProperties](imagick.getimageproperties.md)— Повертає властивості зображення
-   [Imagick::getImageProperty](imagick.getimageproperty.md)— Повертає іменовану властивість зображення
-   [Imagick::getImageRedPrimary](imagick.getimageredprimary.md)— Повертає червону первинну точку кольоровості
-   [Imagick::getImageRegion](imagick.getimageregion.md)— Витягує область зображення
-   [Imagick::getImageRenderingIntent](imagick.getimagerenderingintent.md)— Повертає схему передачі кольору зображення
-   [Imagick::getImageResolution](imagick.getimageresolution.md)— Повертає роздільну здатність зображення за X та Y
-   [Imagick::getImagesBlob](imagick.getimagesblob.md)— Повертає всі послідовності зображення у вигляді великого двійкового об'єкта
-   [Imagick::getImageScene](imagick.getimagescene.md)— Повертає сцену зображення
-   [Imagick::getImageSignature](imagick.getimagesignature.md) \- Генерує хеш SHA-256
-   [Imagick::getImageSize](imagick.getimagesize.md)— Повертає розмір зображення у байтах
-   [Imagick::getImageTicksPerSecond](imagick.getimagetickspersecond.md)— Отримує кількість кадрів на секунду для зображення
-   [Imagick::getImageTotalInkDensity](imagick.getimagetotalinkdensity.md)— Повертає загальну щільність чорнила зображення
-   [Imagick::getImageType](imagick.getimagetype.md)— Повертає можливий тип зображення
-   [Imagick::getImageUnits](imagick.getimageunits.md)— Повертає одиниці вимірювання роздільної здатності зображення
-   [Imagick::getImageVirtualPixelMethod](imagick.getimagevirtualpixelmethod.md)— Повертає метод віртуального пікселя
-   [Imagick::getImageWhitePoint](imagick.getimagewhitepoint.md)— Повертає білу точку кольоровості
-   [Imagick::getImageWidth](imagick.getimagewidth.md)— Повертає ширину зображення
-   [Imagick::getInterlaceScheme](imagick.getinterlacescheme.md)— Отримує схему стиснення зображення
-   [Imagick::getIteratorIndex](imagick.getiteratorindex.md)— Повертає індекс активного поточного зображення.
-   [Imagick::getNumberImages](imagick.getnumberimages.md)— Повертає кількість зображень в об'єкті
-   [Imagick::getOption](imagick.getoption.md)— Повертає значення, пов'язане із зазначеним ключем
-   [Imagick::getPackageName](imagick.getpackagename.md)— Повертає ім'я ImageMagick
-   [Imagick::getPage](imagick.getpage.md)— Повертає геометрію сторінки
-   [Imagick::getPixelIterator](imagick.getpixeliterator.md) \- Повертає MagickPixelIterator
-   [Imagick::getPixelRegionIterator](imagick.getpixelregioniterator.md)— Повертає об'єкт ImagickPixelIterator для секції зображення
-   [Imagick::getPointSize](imagick.getpointsize.md)— Повертає розмір точки
-   [Imagick::getQuantum](imagick.getquantum.md)— Повертає квантовий діапазон ImageMagick
-   [Imagick::getQuantumDepth](imagick.getquantumdepth.md) \- Повертає величину глибини
-   [Imagick::getQuantumRange](imagick.getquantumrange.md)— Повертає розмір спектру Imagick
-   [Imagick::getRegistry](imagick.getregistry.md)— Отримує запис StringRegistry
-   [Imagick::getReleaseDate](imagick.getreleasedate.md)— Повертає дату випуску ImageMagick
-   [Imagick::getResource](imagick.getresource.md)— Повертає розмір пам'яті вказаного ресурсу.
-   [Imagick::getResourceLimit](imagick.getresourcelimit.md)— Повертає заданий ліміт ресурсів
-   [Imagick::getSamplingFactors](imagick.getsamplingfactors.md)— Повертає горизонтальний та вертикальний фактор вибірки
-   [Imagick::getSize](imagick.getsize.md)— Повертає розмір, пов'язаний із об'єктом Imagick
-   [Imagick::getSizeOffset](imagick.getsizeoffset.md)— Повертає розмір усунення
-   [Imagick::getVersion](imagick.getversion.md)— Повертає версію API ImageMagick
-   [Imagick::haldClutImage](imagick.haldclutimage.md)— Замінює кольори у зображенні
-   [Imagick::hasNextImage](imagick.hasnextimage.md)— Перевіряє, чи об'єкт містить більше зображень
-   [Imagick::hasPreviousImage](imagick.haspreviousimage.md)— Перевіряє, чи об'єкт має попереднє зображення.
-   [Imagick::identifyFormat](imagick.identifyformat.md)— Замінює будь-які вбудовані символи форматування відповідною властивістю зображення
-   [Imagick::identifyImage](imagick.identifyimage.md)— Визначає зображення та отримує атрибути
-   [Imagick::implodeImage](imagick.implodeimage.md)— Створює копію зображення
-   [Imagick::importImagePixels](imagick.importimagepixels.md)— Імпортує пікселі зображення
-   [Imagick::inverseFourierTransformImage](imagick.inversefouriertransformimage.md) \- Реалізує дискретне перетворення Фур'є
-   [Imagick::labelImage](imagick.labelimage.md)— Додає позначку до зображення
-   [Imagick::levelImage](imagick.levelimage.md)— Регулює рівні зображення
-   [Imagick::linearStretchImage](imagick.linearstretchimage.md)— Розтягує з насиченням яскравість зображення
-   [Imagick::liquidRescaleImage](imagick.liquidrescaleimage.md)— Анімує зображення чи зображення
-   [Imagick::listRegistry](imagick.listregistry.md)— Перелічує всі налаштування реєстру
-   [Imagick::magnifyImage](imagick.magnifyimage.md)— Пропорційно масштабує зображення вдвічі
-   [Imagick::mapImage](imagick.mapimage.md)— Замінює кольори зображення на найближчий колір із еталонного зображення
-   [Imagick::matteFloodfillImage](imagick.mattefloodfillimage.md)— Змінює значення прозорості кольору
-   [Imagick::medianFilterImage](imagick.medianfilterimage.md)— Застосовує цифровий фільтр
-   [Imagick::mergeImageLayers](imagick.mergeimagelayers.md)— Об'єднує шари зображення
-   [Imagick::minifyImage](imagick.minifyimage.md)— Масштабує зображення пропорційно до половини його розміру.
-   [Imagick::modulateImage](imagick.modulateimage.md)— Керуйте яскравістю, насиченістю та відтінком
-   [Imagick::montageImage](imagick.montageimage.md)— Створює складне зображення
-   [Imagick::morphImages](imagick.morphimages.md)— Перетворює набір зображень
-   [Imagick::morphology](imagick.morphology.md)— Застосовує зображення ядро, надане користувачем, відповідно до заданого методу морфології
-   [Imagick::mosaicImages](imagick.mosaicimages.md)— Формує мозаїку із зображень
-   [Imagick::motionBlurImage](imagick.motionblurimage.md)— Імітує розмиття у русі
-   [Imagick::negateImage](imagick.negateimage.md) \- Інвертує кольори в еталонному зображенні
-   [Imagick::newImage](imagick.newimage.md)— Створює нове зображення
-   [Imagick::newPseudoImage](imagick.newpseudoimage.md)— Створює нове зображення
-   [Imagick::nextImage](imagick.nextimage.md)— Переходить до наступного зображення
-   [Imagick::normalizeImage](imagick.normalizeimage.md)— Підвищує контрастність кольорового зображення
-   [Imagick::oilPaintImage](imagick.oilpaintimage.md)— Імітує картину олією
-   [Imagick::opaquePaintImage](imagick.opaquepaintimage.md)— Змінює значення кольору будь-якого пікселя, що відповідає цільовому
-   [Imagick::optimizeImageLayers](imagick.optimizeimagelayers.md)— Видаляє повторювані частини зображень для оптимізації
-   [Imagick::orderedPosterizeImage](imagick.orderedposterizeimage.md) \- Виконує впорядкований дизеринг
-   [Imagick::paintFloodfillImage](imagick.paintfloodfillimage.md)— Змінює значення кольору будь-якого пікселя, що відповідає меті
-   [Imagick::paintOpaqueImage](imagick.paintopaqueimage.md)— Змінює будь-який піксель, що відповідає кольору
-   [Imagick::paintTransparentImage](imagick.painttransparentimage.md)— Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою
-   [Imagick::pingImage](imagick.pingimage.md)— Отримує основні атрибути зображення
-   [Imagick::pingImageBlob](imagick.pingimageblob.md)— Швидко витягує атрибути
-   [Imagick::pingImageFile](imagick.pingimagefile.md)— Отримує базові атрибути зображення у спрощений спосіб.
-   [Imagick::polaroidImage](imagick.polaroidimage.md) \- Імітує фото Polaroid
-   [Imagick::posterizeImage](imagick.posterizeimage.md)— Зменшує зображення до обмеженої кількості рівнів кольору
-   [Imagick::previewImages](imagick.previewimages.md)— Швидке визначення відповідних параметрів для обробки зображень
-   [Imagick::previousImage](imagick.previousimage.md)— Перехід до попереднього зображення в об'єкті
-   [Imagick::profileImage](imagick.profileimage.md)— Додає або видаляє профіль зображення
-   [Imagick::quantizeImage](imagick.quantizeimage.md) \- Аналізує кольори еталонного зображення
-   [Imagick::quantizeImages](imagick.quantizeimages.md)— Аналізує кольори у послідовності зображень
-   [Imagick::queryFontMetrics](imagick.queryfontmetrics.md)— Повертає масив, який представляє метрики шрифту
-   [Imagick::queryFonts](imagick.queryfonts.md)— Повертає налаштовані шрифти
-   [Imagick::queryFormats](imagick.queryformats.md)— Повертає формати, які підтримує Imagick
-   [Imagick::radialBlurImage](imagick.radialblurimage.md)— Радіальне розмиття зображення
-   [Imagick::raiseImage](imagick.raiseimage.md)— Створює імітацію ефекту 3D-кнопки
-   [Imagick::randomThresholdImage](imagick.randomthresholdimage.md)— Створює висококонтрастне двокольорове зображення
-   [Imagick::readImage](imagick.readimage.md)— Читає зображення із файлу
-   [Imagick::readImageBlob](imagick.readimageblob.md)— Зчитує зображення з двійкового рядка
-   [Imagick::readImageFile](imagick.readimagefile.md)— Читає зображення із відкритого дескриптора файлу
-   [Imagick::readimages](imagick.readimages.md)— Читає зображення з масиву імен файлів
-   [Imagick::recolorImage](imagick.recolorimage.md)— Перефарбовує зображення
-   [Imagick::reduceNoiseImage](imagick.reducenoiseimage.md)— Згладжує контури зображення
-   [Imagick::remapImage](imagick.remapimage.md)— Перезначає кольори зображення
-   [Imagick::removeImage](imagick.removeimage.md)— Видалення зображення зі списку зображень
-   [Imagick::removeImageProfile](imagick.removeimageprofile.md)— Видаляє іменований профіль зображення та повертає його
-   [Imagick::render](imagick.render.md) \- Відображає всі попередні команди малювання
-   [Imagick::resampleImage](imagick.resampleimage.md)— Перетворює зображення до потрібної роздільної здатності
-   [Imagick::resetImagePage](imagick.resetimagepage.md)— Скидає сторінку зображення
-   [Imagick::resizeImage](imagick.resizeimage.md)— Масштабує зображення
-   [Imagick::rollImage](imagick.rollimage.md)— Зміщує зображення
-   [Imagick::rotateImage](imagick.rotateimage.md)— Повертає зображення
-   [Imagick::rotationalBlurImage](imagick.rotationalblurimage.md)— Застосовує обертальне розмиття до зображення.
-   [Imagick::roundCorners](imagick.roundcorners.md)— Заокруглює кути зображення
-   [Imagick::sampleImage](imagick.sampleimage.md)— Масштабує зображення з піксельною вибіркою
-   [Imagick::scaleImage](imagick.scaleimage.md)— Масштабує розмір зображення
-   [Imagick::segmentImage](imagick.segmentimage.md)— Сегментує зображення
-   [Imagick::selectiveBlurImage](imagick.selectiveblurimage.md) \- Вибіркове розмиття зображення в межах порогового значення контрастності
-   [Imagick::separateImageChannel](imagick.separateimagechannel.md)— Відокремлює канал від зображення
-   [Imagick::sepiaToneImage](imagick.sepiatoneimage.md)— Тонування зображення сепією
-   [Imagick::setBackgroundColor](imagick.setbackgroundcolor.md)— Встановлює колір тла об'єкта за промовчанням
-   [Imagick::setColorspace](imagick.setcolorspace.md)— Встановлює колірний простір
-   [Imagick::setCompression](imagick.setcompression.md)— Встановлює тип стиснення об'єкта за промовчанням
-   [Imagick::setCompressionQuality](imagick.setcompressionquality.md)— Встановлює якість стандартного стиснення об'єкта
-   [Imagick::setFilename](imagick.setfilename.md)— Встановлює ім'я файлу перед читанням чи записом зображення
-   [Imagick::setFirstIterator](imagick.setfirstiterator.md) \- Встановлює ітератор Imagick для першого зображення
-   [Imagick::setFont](imagick.setfont.md) \- Встановлює шрифт
-   [Imagick::setFormat](imagick.setformat.md)— Встановлює формат об'єкту Imagick
-   [Imagick::setGravity](imagick.setgravity.md) \- Встановлює гравітацію
-   [Imagick::setImage](imagick.setimage.md)— Замінює зображення в об'єкті
-   [Imagick::setImageAlphaChannel](imagick.setimagealphachannel.md) \- Встановлює альфа-канал зображення
-   [Imagick::setImageArtifact](imagick.setimageartifact.md)— Встановлює артефакт зображення
-   [Imagick::setImageAttribute](imagick.setimageattribute.md)— Встановлює атрибут зображення
-   [Imagick::setImageBackgroundColor](imagick.setimagebackgroundcolor.md)— Встановлює колір тла зображення
-   [Imagick::setImageBias](imagick.setimagebias.md)— Встановлює зміщення зображення для будь-якого методу, який згортає зображення
-   [Imagick::setImageBiasQuantum](imagick.setimagebiasquantum.md)— Встановлює зміщення зображення
-   [Imagick::setImageBluePrimary](imagick.setimageblueprimary.md)— Встановлює кольоровість зображення блакитною основною точкою.
-   [Imagick::setImageBorderColor](imagick.setimagebordercolor.md)— Встановлює колір рамки зображення
-   [Imagick::setImageChannelDepth](imagick.setimagechanneldepth.md)— Встановлює глибину певного каналу зображення
-   [Imagick::setImageClipMask](imagick.setimageclipmask.md) \- Встановлює маску кліпу
-   [Imagick::setImageColormapColor](imagick.setimagecolormapcolor.md)— Встановлює колір вказаного індексу картки
-   [Imagick::setImageColorspace](imagick.setimagecolorspace.md)— Встановлює колірний простір зображення
-   [Imagick::setImageCompose](imagick.setimagecompose.md)— Встановлює оператор складеного зображення
-   [Imagick::setImageCompression](imagick.setimagecompression.md)— Встановлює стиснення зображення
-   [Imagick::setImageCompressionQuality](imagick.setimagecompressionquality.md)— Встановлює якість стиснення зображення
-   [Imagick::setImageDelay](imagick.setimagedelay.md)— Встановлює затримку зображення
-   [Imagick::setImageDepth](imagick.setimagedepth.md)— Встановлює глибину зображення
-   [Imagick::setImageDispose](imagick.setimagedispose.md)— Встановлює метод видалення зображення
-   [Imagick::setImageExtent](imagick.setimageextent.md)— Встановлює розмір зображення
-   [Imagick::setImageFilename](imagick.setimagefilename.md)— Встановлює ім'я конкретного файлу.
-   [Imagick::setImageFormat](imagick.setimageformat.md)— Встановлює формат певного зображення
-   [Imagick::setImageGamma](imagick.setimagegamma.md)— Встановлює гаму зображення
-   [Imagick::setImageGravity](imagick.setimagegravity.md)— Встановлює гравітацію зображення
-   [Imagick::setImageGreenPrimary](imagick.setimagegreenprimary.md)— Встановлює кольоровість зображення зеленою первинною точкою.
-   [Imagick::setImageIndex](imagick.setimageindex.md) \- Встановлює позицію ітератора
-   [Imagick::setImageInterlaceScheme](imagick.setimageinterlacescheme.md)— Встановлює стиснення зображення
-   [Imagick::setImageInterpolateMethod](imagick.setimageinterpolatemethod.md)— Встановлює метод інтерполяції пікселів зображення
-   [Imagick::setImageIterations](imagick.setimageiterations.md)— Встановлює ітерацію зображення
-   [Imagick::setImageMatte](imagick.setimagematte.md)— Встановлює матовий канал зображення
-   [Imagick::setImageMatteColor](imagick.setimagemattecolor.md)— Встановлює матовий колір зображення
-   [Imagick::setImageOpacity](imagick.setimageopacity.md)— Встановлює рівень непрозорості зображення
-   [Imagick::setImageOrientation](imagick.setimageorientation.md)— Встановлює орієнтацію зображення
-   [Imagick::setImagePage](imagick.setimagepage.md)— Встановлює геометрію сторінки зображення
-   [Imagick::setImageProfile](imagick.setimageprofile.md) \- Додає іменований профіль до об'єкту Imagick
-   [Imagick::setImageProperty](imagick.setimageproperty.md)— Встановлює властивість зображення
-   [Imagick::setImageRedPrimary](imagick.setimageredprimary.md)— Встановлює червону первинну точку кольоровості зображення
-   [Imagick::setImageRenderingIntent](imagick.setimagerenderingintent.md)— Встановлює схему передачі кольору зображення
-   [Imagick::setImageResolution](imagick.setimageresolution.md)— Встановлює роздільну здатність зображення
-   [Imagick::setImageScene](imagick.setimagescene.md)— Встановлює сцену зображення
-   [Imagick::setImageTicksPerSecond](imagick.setimagetickspersecond.md)— Встановлює тривалість відображення кадру
-   [Imagick::setImageType](imagick.setimagetype.md)— Встановлює тип зображення
-   [Imagick::setImageUnits](imagick.setimageunits.md)— Встановлює одиниці вимірювання роздільної здатності зображення
-   [Imagick::setImageVirtualPixelMethod](imagick.setimagevirtualpixelmethod.md) \- Встановлює метод віртуального пікселя
-   [Imagick::setImageWhitePoint](imagick.setimagewhitepoint.md)— Встановлює білу точку кольору зображення
-   [Imagick::setInterlaceScheme](imagick.setinterlacescheme.md)— Встановлює стиснення зображення
-   [Imagick::setIteratorIndex](imagick.setiteratorindex.md) \- Встановлює позицію ітератора
-   [Imagick::setLastIterator](imagick.setlastiterator.md) \- Встановлює ітератор Imagick до останнього зображення
-   [Imagick::setOption](imagick.setoption.md) \- Встановлює опцію
-   [Imagick::setPage](imagick.setpage.md)— Встановлює геометрію сторінки об'єкту Imagick
-   [Imagick::setPointSize](imagick.setpointsize.md) \- Встановлює розмір точки
-   [Imagick::setProgressMonitor](imagick.setprogressmonitor.md)— Встановлює callback-функцію, яка буде викликатись під час обробки зображення Imagick
-   [Imagick::setRegistry](imagick.setregistry.md)— Встановлює значення запису реєстру ImageMagick з ім'ям key
-   [Imagick::setResolution](imagick.setresolution.md)— Встановлює роздільну здатність зображення
-   [Imagick::setResourceLimit](imagick.setresourcelimit.md) \- Встановлює ліміт для конкретного ресурсу
-   [Imagick::setSamplingFactors](imagick.setsamplingfactors.md)— Встановлює коефіцієнти вибірки зображень
-   [Imagick::setSize](imagick.setsize.md)— Встановлює розмір об'єкту Imagick
-   [Imagick::setSizeOffset](imagick.setsizeoffset.md)— Встановлює розмір та усунення об'єкта Imagick
-   [Imagick::setType](imagick.settype.md)— Встановлює атрибут типу зображення
-   [Imagick::shadeImage](imagick.shadeimage.md)— Створює 3D-ефект
-   [Imagick::shadowImage](imagick.shadowimage.md)— Імітує тінь зображення
-   [Imagick::sharpenImage](imagick.sharpenimage.md)— Підвищує різкість зображення
-   [Imagick::shaveImage](imagick.shaveimage.md)— Видаляє пікселі по краях зображення
-   [Imagick::shearImage](imagick.shearimage.md) \- Створює паралелограм
-   [Imagick::sigmoidalContrastImage](imagick.sigmoidalcontrastimage.md) \- Регулює контраст зображення
-   [Imagick::sketchImage](imagick.sketchimage.md) \- Імітує малюнок олівцем
-   [Imagick::smushImages](imagick.smushimages.md)— Бере всі зображення з поточного покажчика зображення до кінця списку зображень і переміщує їх
-   [Imagick::solarizeImage](imagick.solarizeimage.md)— Застосовує до зображення ефект соляризації
-   [Imagick::sparseColorImage](imagick.sparsecolorimage.md) \- Інтерполює кольори
-   [Imagick::spliceImage](imagick.spliceimage.md)— Склеює суцільний колір у зображення
-   [Imagick::spreadImage](imagick.spreadimage.md)— Випадково зміщує кожен піксель у блоці
-   [Imagick::statisticImage](imagick.statisticimage.md)— Модифікація зображення за допомогою функції статистики
-   [Imagick::steganoImage](imagick.steganoimage.md)— Приховує цифровий водяний знак у зображенні
-   [Imagick::stereoImage](imagick.stereoimage.md)— Об'єднує два зображення
-   [Imagick::stripImage](imagick.stripimage.md)— Знімає зображення всіх профілів та коментарів
-   [Imagick::subImageMatch](imagick.subimagematch.md)— Виконує пошук фрагмента зображення у поточному зображенні та повертає другорядне зображення.
-   [Imagick::swirlImage](imagick.swirlimage.md)— Закручує пікселі навколо центру зображення
-   [Imagick::textureImage](imagick.textureimage.md)— Багато разів розміщує зображення текстури
-   [Imagick::thresholdImage](imagick.thresholdimage.md) \- Змінює окремі пікселі на основі порогового значення
-   [Imagick::thumbnailImage](imagick.thumbnailimage.md)— Змінює розмір зображення
-   [Imagick::tintImage](imagick.tintimage.md)— Застосовує вектор кольору до кожного пікселя зображення
-   [Imagick::\_\_function toString() { \[native code\] }](imagick.tostring.md)— Повертає зображення у вигляді рядка
-   [Imagick::transformImage](imagick.transformimage.md)— Зручний метод налаштування розміру кадрування та геометрії зображення
-   [Imagick::transformImageColorspace](imagick.transformimagecolorspace.md)— Перетворює зображення на новий колірний простір
-   [Imagick::transparentPaintImage](imagick.transparentpaintimage.md)— Малює пікселі прозорими
-   [Imagick::transposeImage](imagick.transposeimage.md)— Створює вертикальне дзеркальне відображення
-   [Imagick::transverseImage](imagick.transverseimage.md)— Створює горизонтальне дзеркальне відображення
-   [Imagick::trimImage](imagick.trimimage.md)— Видаляє краї із зображення
-   [Imagick::uniqueImageColors](imagick.uniqueimagecolors.md) \- Відкидає все, крім одного, будь-якого кольору пікселя
-   [Imagick::unsharpMaskImage](imagick.unsharpmaskimage.md) \- Різкість зображення
-   [Imagick::valid](imagick.valid.md)— Перевіряє, чи поточний елемент є коректним.
-   [Imagick::vignetteImage](imagick.vignetteimage.md)— Додає він'єтний фільтр до зображення
-   [Imagick::waveImage](imagick.waveimage.md)— Застосовує хвильовий фільтр до зображення
-   [Imagick::whiteThresholdImage](imagick.whitethresholdimage.md)— Зафарбовує всі пікселі вище за поріг у білий
-   [Imagick::writeImage](imagick.writeimage.md)— Записує зображення за вказаним ім'ям файлу
-   [Imagick::writeImageFile](imagick.writeimagefile.md)— Записує зображення у файл
-   [Imagick::writeImages](imagick.writeimages.md)— Записує зображення або послідовність зображень
-   [Imagick::writeImagesFile](imagick.writeimagesfile.md)— Записує кадри у файловий дескриптор
