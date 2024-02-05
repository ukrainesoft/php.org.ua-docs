---
navigation:
  - ref.exif.md: « Exif Функції
  - function.exif-read-data.md: exif\_read\_data »
  - index.md: PHP Manual
  - ref.exif.md: Exif Функції
title: exif\_imagetype
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exif\_imagetype

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

exif\_imagetype — Determine the type of an image

### Опис

```methodsynopsis
exif_imagetype(string $filename): int|false
```

**exif\_imagetype()** зчитує початкові байти зображення та перевіряє їх сигнатуру.

**exif\_imagetype()** може використовуватися, щоб уникнути інших викликів [exif-функцій](ref.exif.md) з непідтримуваними аргументами. Також при взаємодії з [$\_SERVER\['HTTP\_ACCEPT'\]](reserved.variables.server.md) можна перевіряти, чи зображення відображатиметься у браузері.

### Список параметрів

`filename`

Зображення, тип якого потрібно визначити.

### Значення, що повертаються

Якщо виявлено коректну сигнатуру, функція поверне відповідну типу зображення константу. Інакше функція поверне **`false`**. Значення, що повертається те ж, що і в другому аргументі при поверненні з функції [getimagesize()](function.getimagesize.md), однак **exif\_imagetype()** значно швидше.

Наступні певні константи представляють можливі значення функції, що повертаються **exif\_imagetype()** :

**Константи Imagetype**

| Значение | Константа |
| --- | --- |
|  | **`IMAGETYPE_GIF`** |
|  | **`IMAGETYPE_JPEG`** |
| 3 | **`IMAGETYPE_PNG`** |
| 4 | **`IMAGETYPE_SWF`** |
| 5 | **`IMAGETYPE_PSD`** |
| 6 | **`IMAGETYPE_BMP`** |
| 7 | **`IMAGETYPE_TIFF_II`** (порядок байт intel) |
| 8 | **`IMAGETYPE_TIFF_MM`** (Порядок байт motorola) |
| 9 | **`IMAGETYPE_JPC`** |
| 10 | **`IMAGETYPE_JP2`** |
| 11 | **`IMAGETYPE_JPX`** |
| 12 | **`IMAGETYPE_JB2`** |
| 13 | **`IMAGETYPE_SWC`** |
| 14 | **`IMAGETYPE_IFF`** |
| 15 | **`IMAGETYPE_WBMP`** |
| 16 | **`IMAGETYPE_XBM`** |
| 17 | **`IMAGETYPE_ICO`** |
| 18 | **`IMAGETYPE_WEBP`** |
| 19 | **`IMAGETYPE_AVIF`** |

> **Зауваження** :
> 
> В случаях, когда невозможно считать количество байтов из файла достаточное для определения типа изображения, функция**exif\_imagetype()** викличе попередження рівня **`E_NOTICE`** і поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Додано підтримку AVIF. |
| 7.1.0 | Додано підтримку WebP. |

### Приклади

**Пример #1 Пример использования**exif\_imagetype()\*\*\*\*

```php
<?php
if (exif_imagetype('image.gif') != IMAGETYPE_GIF) {
    echo 'Картинка не gif';
}
?>
```

### Дивіться також

-   [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) \- Отримання Mime-типу для типу зображення, що повертається функціями getimagesize, exif\_read\_data, exif\_thumbnail, exif\_imagetype
-   [getimagesize()](function.getimagesize.md) \- Отримання розміру зображення
