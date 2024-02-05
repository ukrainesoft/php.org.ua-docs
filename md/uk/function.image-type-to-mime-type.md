---
navigation:
  - function.image-type-to-extension.md: « image\_type\_to\_extension
  - function.image2wbmp.md: image2wbmp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: image\_type\_to\_mime\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# image\_type\_to\_mime\_type

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

image\_type\_to\_mime\_type — Отримання типу Mime для типу зображення, що повертається функціями getimagesize, exif\_read\_data, exif\_thumbnail, exif\_imagetype

### Опис

```methodsynopsis
image_type_to_mime_type(int $image_type): string
```

Функция**image\_type\_to\_mime\_type()** визначає Mime-тип для константи IMAGETYPE.

### Список параметрів

`image_type`

Одна из констант`IMAGETYPE_XXX`

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
| **`IMAGETYPE_AVIF`** | `image/avif` |

### Приклади

**Приклад #1 Приклад використання** image\_type\_to\_mime\_type()\*\*\*\*

```php
<?php
header("Content-type: " . image_type_to_mime_type(IMAGETYPE_PNG));
?>
```

### Примітки

> **Зауваження** :
> 
> Ця функція не потребує бібліотеки GD.

### Дивіться також

-   [getimagesize()](function.getimagesize.md) \- Отримання розміру зображення
-   [exif\_imagetype()](function.exif-imagetype.md) \- Determine the type of an image
-   [exif\_read\_data()](function.exif-read-data.md) \- Читає заголовки EXIF ​​із файлів зображень
-   [exif\_thumbnail()](function.exif-thumbnail.md) \- Отримує вбудоване прев'ю зображення
