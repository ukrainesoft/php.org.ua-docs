---
navigation:
  - function.image-type-to-extension.md: « imagetypeтоextension
  - function.image2wbmp.md: image2wbmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagetypeтоmimetype
---
# imagetypeтоmimetype

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

imagetypeтоmimetype — Отримання типу Mime для типу зображення, що повертається функціями getimagesize, exifreaddata, exifthumbnail, exifimagetype

### Опис

```methodsynopsis
image_type_to_mime_type(int $image_type): string
```

Функція **imagetypeтоmimetype()** визначає Mime-тип для константи IMAGETYPE.

### Список параметрів

`image_type`

Одна з констант `IMAGETYPE_XXX`

### Значення, що повертаються

Значення, що повертаються наведені нижче

**Значення, що повертаються і Константи**

| `image_type` | Возвращаемое значение |
| --- | --- |
| **`IMAGETYPE_GIF`** | `image/gif` |
| **`IMAGETYPE_JPEG`** | `image/jpeg` |
| **`IMAGETYPE_PNG`** | `image/png` |
| **`IMAGETYPE_SWF`** | `application/x-shockwave-flash` |
| **`IMAGETYPE_PSD`** | `image/psd` |
| **`IMAGETYPE_BMP`** | `image/bmp` |
| **`IMAGETYPE_TIFF_II`** (порядок байт intel) | `image/tiff` |
| **`IMAGETYPE_TIFF_MM`** (Порядок байт motorola) | `image/tiff` |
| **`IMAGETYPE_JPC`** | `application/octet-stream` |
| **`IMAGETYPE_JP2`** | `image/jp2` |
| **`IMAGETYPE_JPX`** | `application/octet-stream` |
| **`IMAGETYPE_JB2`** | `application/octet-stream` |
| **`IMAGETYPE_SWC`** | `application/x-shockwave-flash` |
| **`IMAGETYPE_IFF`** | `image/iff` |
| **`IMAGETYPE_WBMP`** | `image/vnd.wap.wbmp` |
| **`IMAGETYPE_XBM`** | `image/xbm` |
| **`IMAGETYPE_ICO`** | `image/vnd.microsoft.icon` |
| **`IMAGETYPE_WEBP`** | `image/webp` |

### Приклади

**Приклад #1 Приклад використання **imagetypeтоmimetype()****

```php
<?php
header("Content-type: " . image_type_to_mime_type(IMAGETYPE_PNG));
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не потребує бібліотеки GD.

### Дивіться також

-   [getimagesize()](function.getimagesize.md) - Отримання розміру зображення
-   [exifimagetype()](function.exif-imagetype.md) - Визначте тип зображення.
-   [exifreaddata()](function.exif-read-data.md) - Читає заголовки EXIF ​​із файлів зображень
-   [exifthumbnail()](function.exif-thumbnail.md) - Отримує вбудоване прев'ю зображення
