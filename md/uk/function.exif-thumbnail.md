Отримує вбудоване прев'ю зображення

-   [« exif\_tagname](function.exif-tagname.html)
    
-   [read\_exif\_data »](function.read-exif-data.html)
    
-   [PHP Manual](index.html)
    
-   [Exif Функции](ref.exif.html)
    
-   Отримує вбудоване прев'ю зображення
    

# exifthumbnail

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

exifthumbnail — Отримує вбудоване зображення.

### Опис

```methodsynopsis
exif_thumbnail(    resource|string $file,    int &$width = null,    int &$height = null,    int &$image_type = null): string|false
```

**exifthumbnail()** зчитує вбудоване прев'ю зображення.

Якщо ви хочете отримати ескіз за допомогою цієї функції, вам необхідно надіслати mimetype-інформацію, використовуючи [header()](function.header.html) функцію.

Іноді **exifthumbnail()** не може створити зображення, але може визначити його розмір. У таких випадках вона повертає **`false`**, але ставить аргументи `width` і `height` правильні значення.

### Список параметрів

`file`

Розташування файлу із зображенням. Можливо як шляхом до файлу, і потоковим ресурсом.

`width`

Ширина ескізу, що повертається.

`height`

Висота ескізу, що повертається.

`image_type`

Тип ескізу, що повертається. Це або TIFF або JPEG.

### Значення, що повертаються

Повертає вбудований ескіз або **`false`**, якщо зображення не містить ескізу.

### список змін

| Версия | Описание                                                                                                   |
|--------|------------------------------------------------------------------------------------------------------------|
|        | Параметр `file` перейменований на `stream` і може приймати як локальний шлях до файлу, і потоковий ресурс. |

### Приклади

**Приклад #1 Приклад використання **exifthumbnail()****

```php
<?php
$image = exif_thumbnail('/path/to/image.jpg', $width, $height, $type);

if ($image!==false) {
    header('Content-type: ' .image_type_to_mime_type($type));
    echo $image;
    exit;
} else {
    // нет доступного превью, здесь можно обработать ошибку
    echo 'Нет доступного эскиза';
}
?>
```

### Примітки

> **Зауваження**
> 
> Якщо параметр `file` використаний передачі потоку у функцію, цей потік може бути перемотується. Зверніть увагу, що файловий позиційний покажчик не буде змінено після завершення роботи цієї функції.

### Дивіться також

-   [exif\_read\_data()](function.exif-read-data.html) - Читає заголовки EXIF ​​із файлів зображень
-   [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.html) - Отримання Mime-типу для типу зображення, що повертається функціями getimagesize, exifreaddata, exifthumbnail, exifimagetype