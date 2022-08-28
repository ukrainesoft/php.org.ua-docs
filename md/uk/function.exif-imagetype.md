Визначення типу зображення

-   [« Exif Функции](ref.exif.html)
    
-   [exif\_read\_data »](function.exif-read-data.html)
    
-   [PHP Manual](index.html)
    
-   [Exif Функции](ref.exif.html)
    
-   Визначення типу зображення
    

# exifimagetype

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

exifimagetype — Визначте type of an image

### Опис

```methodsynopsis
exif_imagetype(string $filename): int|false
```

**exifimagetype()** зчитує початкові байти зображення та перевіряє їх сигнатуру.

**exifimagetype()** може використовуватися, щоб уникнути інших викликів [exif-функций](ref.exif.html) з непідтримуваними аргументами. Також при взаємодії з [$\_SERVER\['HTTP\_ACCEPT'\]](reserved.variables.server.html) можна перевіряти, чи зображення відображатиметься у браузері.

### Список параметрів

`filename`

Зображення, тип якого потрібно визначити.

### Значення, що повертаються

Якщо виявлено коректну сигнатуру, функція поверне відповідну типу зображення константу. Інакше функція поверне **`false`**. Значення, що повертається те ж, що і в другому аргументі при поверненні з функції [getimagesize()](function.getimagesize.html), однак **exifimagetype()** значно швидше.

Наступні певні константи представляють можливі значення функції, що повертаються **exifimagetype()**

**Константи Imagetype**

| Значение | Константа |
| --- | --- |
|  | **`IMAGETYPE_GIF`** |
|  | **`IMAGETYPE_JPEG`** |
|  | **`IMAGETYPE_PNG`** |
|  | **`IMAGETYPE_SWF`** |
|  | **`IMAGETYPE_PSD`** |
|  | **`IMAGETYPE_BMP`** |
|  | **`IMAGETYPE_TIFF_II`** (порядок байт intel) |
|  | **`IMAGETYPE_TIFF_MM`** (Порядок байт motorola) |
|  | **`IMAGETYPE_JPC`** |
|  | **`IMAGETYPE_JP2`** |
|  | **`IMAGETYPE_JPX`** |
|  | **`IMAGETYPE_JB2`** |
|  | **`IMAGETYPE_SWC`** |
|  | **`IMAGETYPE_IFF`** |
|  | **`IMAGETYPE_WBMP`** |
|  | **`IMAGETYPE_XBM`** |
|  | **`IMAGETYPE_ICO`** |
|  | **`IMAGETYPE_WEBP`** |

> **Зауваження**
> 
> У випадках, коли неможливо рахувати кількість байтів із файлу достатню для визначення типу зображення, функція **exifimagetype()** викличе попередження рівня **`E_NOTICE`** і поверне **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано підтримку WebP. |

### Приклади

**Приклад #1 Приклад використання **exifimagetype()****

```php
<?php
if (exif_imagetype('image.gif') != IMAGETYPE_GIF) {
    echo 'Картинка не gif';
}
?>
```

### Дивіться також

-   [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.html) - Отримання Mime-типу для типу зображення, що повертається функціями getimagesize, exifreaddata, exifthumbnail, exifimagetype
-   [getimagesize()](function.getimagesize.html) - Отримання розміру зображення