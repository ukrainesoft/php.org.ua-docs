---
navigation:
  - image.resources.md: « Типи ресурсів
  - image.examples.md: Приклади »
  - index.md: PHP Manual
  - book.image.md: GD
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`GD_VERSION`**(string)

Версія GD, з якою було скомпільовано PHP.

**`GD_MAJOR_VERSION`**(int)

Повнофункціональна версія GD, з якою був скомпільований PHP.

**`GD_MINOR_VERSION`**(int)

Скорочена версія GD, з якою був скомпільований PHP.

**`GD_RELEASE_VERSION`**(int)

Робоча версія GD, з якою було скомпільовано PHP.

**`GD_EXTRA_VERSION`**(string)

Додаткова (beta/rc..) версія GD, з якою був скомпільований PHP.

**`GD_BUNDLED`**(int)

Якщо використовується версія GD, що розповсюджується з PHP, константа приймає значення 1, в іншому випадку 0.

**`IMG_AVIF`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md). (Доступно, починаючи з PHP 8.1.0)

**`IMG_BMP`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_GIF`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_JPG`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_JPEG`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

> **Зауваження** :
> 
> Ця константа має те саме значення, що і **`IMG_JPG`**

**`IMG_PNG`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_WBMP`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_XPM`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)

**`IMG_WEBP`**(int)

Повертається як значення функції [imagetypes()](function.imagetypes.md)(Доступно с PHP 7.0.10)

**`IMG_WEBP_LOSSLESS`**(int)

. (Доступно, починаючи з PHP 8.1.0)

**`IMG_COLOR_TILED`**(int)

Спеціальний варіант кольору, який може бути використаний замість певного за допомогою [imagecolorallocate()](function.imagecolorallocate.md) і [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

**`IMG_COLOR_STYLED`**(int)

Спеціальний варіант кольору, який може бути використаний замість певного за допомогою [imagecolorallocate()](function.imagecolorallocate.md) і [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

**`IMG_COLOR_BRUSHED`**(int)

Спеціальний варіант кольору, який може бути використаний замість певного за допомогою [imagecolorallocate()](function.imagecolorallocate.md) і [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

**`IMG_COLOR_STYLEDBRUSHED`**(int)

Спеціальний варіант кольору, який може бути використаний замість певного за допомогою [imagecolorallocate()](function.imagecolorallocate.md) і [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

**`IMG_COLOR_TRANSPARENT`**(int)

Спеціальний варіант кольору, який може бути використаний замість певного за допомогою [imagecolorallocate()](function.imagecolorallocate.md) і [imagecolorallocatealpha()](function.imagecolorallocatealpha.md)

**`IMG_AFFINE_TRANSLATE`**(int)

Константа типу афінного перетворення; константу вказують як значення аргументу функції [imageaffinematrixget()](function.imageaffinematrixget.md)

**`IMG_AFFINE_SCALE`**(int)

Константа типу афінного перетворення; константу вказують як значення аргументу функції [imageaffinematrixget()](function.imageaffinematrixget.md)

**`IMG_AFFINE_ROTATE`**(int)

Константа типу афінного перетворення; константу вказують як значення аргументу функції [imageaffinematrixget()](function.imageaffinematrixget.md)

**`IMG_AFFINE_SHEAR_HORIZONTAL`**(int)

Константа типу афінного перетворення; константу вказують як значення аргументу функції [imageaffinematrixget()](function.imageaffinematrixget.md)

**`IMG_AFFINE_SHEAR_VERTICAL`**(int)

Константа типу афінного перетворення; константу вказують як значення аргументу функції [imageaffinematrixget()](function.imageaffinematrixget.md)

**`IMG_ARC_ROUNDED`**(int)

Константа стилю, константу вказують як значення аргументу функції [imagefilledarc()](function.imagefilledarc.md)

> **Зауваження** :
> 
> Ця константа має те саме значення, що і **`IMG_ARC_PIE`**

**`IMG_ARC_PIE`**(int)

Константа стилю, константу вказують як значення аргументу функції [imagefilledarc()](function.imagefilledarc.md)

**`IMG_ARC_CHORD`**(int)

Константа стилю, константу вказують як значення аргументу функції [imagefilledarc()](function.imagefilledarc.md)

**`IMG_ARC_NOFILL`**(int)

Константа стилю, константу вказують як значення аргументу функції [imagefilledarc()](function.imagefilledarc.md)

**`IMG_ARC_EDGED`**(int)

Константа стилю, константу вказують як значення аргументу функції [imagefilledarc()](function.imagefilledarc.md)

**`IMG_GD2_RAW`**(int)

Константа типу, константу вказують як значення аргументу функції [imagegd2()](function.imagegd2.md)

**`IMG_GD2_COMPRESSED`**(int)

Константа типу, константу вказують як значення аргументу функції [imagegd2()](function.imagegd2.md)

**`IMG_EFFECT_REPLACE`**(int)

Ефект альфа-змішування, константу вказують як значення аргументу функції [imagelayereffect()](function.imagelayereffect.md)

**`IMG_EFFECT_ALPHABLEND`**(int)

Ефект альфа-змішування, константу вказують як значення аргументу функції [imagelayereffect()](function.imagelayereffect.md)

**`IMG_EFFECT_NORMAL`**(int)

Ефект альфа-змішування, константу вказують як значення аргументу функції [imagelayereffect()](function.imagelayereffect.md)

**`IMG_EFFECT_OVERLAY`**(int)

Ефект альфа-змішування, константу вказують як значення аргументу функції [imagelayereffect()](function.imagelayereffect.md)

**`IMG_EFFECT_MULTIPLY`**(int)

Ефект альфа-змішування, константу вказують як значення аргументу функції [imagelayereffect()](function.imagelayereffect.md)

**`IMG_FILTER_NEGATE`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_GRAYSCALE`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_BRIGHTNESS`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_CONTRAST`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_COLORIZE`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_EDGEDETECT`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_GAUSSIAN_BLUR`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_SELECTIVE_BLUR`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_EMBOSS`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_MEAN_REMOVAL`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_SMOOTH`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_PIXELATE`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)

**`IMG_FILTER_SCATTER`**(int)

Спеціальний фільтр GD, константу вказують як значення аргументу функції [imagefilter()](function.imagefilter.md)(Доступна с PHP 7.4.0)

**`IMAGETYPE_GIF`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JPEG`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JPEG2000`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_PNG`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_SWF`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_PSD`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_BMP`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_WBMP`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_XBM`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_TIFF_II`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_TIFF_MM`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_IFF`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JB2`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JPC`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JP2`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_JPX`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_SWC`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_ICO`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md)

**`IMAGETYPE_WEBP`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md). (Доступно, починаючи з PHP 7.1.0)

**`IMAGETYPE_AVIF`**(int)

Константа типу зображення, константу вказують як значення аргументу функцій [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) і [image\_type\_to\_extension()](function.image-type-to-extension.md). (Доступно, починаючи з PHP 8.1.0)

**`PNG_NO_FILTER`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_FILTER_NONE`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_FILTER_SUB`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_FILTER_UP`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_FILTER_AVG`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_FILTER_PAETH`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`PNG_ALL_FILTERS`**(int)

Спеціальний фільтр PNG filter, константу вказують як значення аргументу функції [imagepng()](function.imagepng.md)

**`IMG_FLIP_VERTICAL`**(int)

Константу вказують як значення аргументу функції [imageflip()](function.imageflip.md)доступна з PHP 5.5.0.

**`IMG_FLIP_HORIZONTAL`**(int)

Константу вказують як значення аргументу функції [imageflip()](function.imageflip.md)доступна з PHP 5.5.0.

**`IMG_FLIP_BOTH`**(int)

Константу вказують як значення аргументу функції [imageflip()](function.imageflip.md)доступна з PHP 5.5.0.

**`IMG_BELL`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BESSEL`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BILINEAR_FIXED`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BICUBIC_FIXED`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BICUBIC`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BLACKMAN`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BOX`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_BSPLINE`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_CATMULLROM`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_GAUSSIAN`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_GENERALIZED_CUBIC`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_HERMITE`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_HAMMING`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_HANNING`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_MITCHELL`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_POWER`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_QUADRATIC`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_SINC`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_NEAREST_NEIGHBOUR`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_WEIGHTED4`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.

**`IMG_TRIANGLE`**(int)

Константу вказують як значення аргументу функції [imagesetinterpolation()](function.imagesetinterpolation.md)доступна з PHP 5.5.0.
