---
navigation:
  - function.exif-tagname.md: « exif\_tagname
  - function.read-exif-data.md: read\_exif\_data »
  - index.md: PHP Manual
  - ref.exif.md: Exif Функції
title: exif\_thumbnail
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exif\_thumbnail

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

exif\_thumbnail — Отримує вбудоване прев'ю зображення

### Опис

```methodsynopsis
exif_thumbnail(    resource|string $file,    int &$width = null,    int &$height = null,    int &$image_type = null): string|false
```

**exif\_thumbnail()** зчитує вбудоване прев'ю зображення.

Якщо ви хочете отримати ескіз за допомогою цієї функції, вам необхідно надіслати mimetype-інформацію, використовуючи [header()](function.header.md)функцию.

Иногда**exif\_thumbnail()** не може створити зображення, але може визначити його розмір. У таких випадках вона повертає **`false`**, але ставить аргументи `width`и`height` правильні значення.

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

| Версия | Опис |
| --- | --- |
| 7.2.0 | Параметр`file`перейменований на`stream` і може приймати як локальний шлях до файлу, і потоковий ресурс. |

### Приклади

**Приклад #1 Приклад використання** exif\_thumbnail()\*\*\*\*

```php
<?php
$image = exif_thumbnail('/path/to/image.jpg', $width, $height, $type);

if ($image!==false) {
    header('Content-type: ' .image_type_to_mime_type($type));
    echo $image;
    exit;
} else {
    // нет доступного превью, здесь можно обработать ошибку
    echo 'Нет доступного эскиза';
}
?>
```

### Примітки

> **Зауваження** :
> 
> Якщо параметр `file` використаний передачі потоку в функцію, цей потік може бути перемотується. Зверніть увагу, що файловий позиційний покажчик не буде змінено після завершення роботи цієї функції.

### Дивіться також

-   [exif\_read\_data()](function.exif-read-data.md) \- Читає заголовки EXIF ​​із файлів зображень
-   [image\_type\_to\_mime\_type()](function.image-type-to-mime-type.md) \- Отримання Mime-типу для типу зображення, що повертається функціями getimagesize, exif\_read\_data, exif\_thumbnail, exif\_imagetype
