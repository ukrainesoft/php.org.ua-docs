---
navigation:
  - function.exif-read-data.md: « exif\_read\_data
  - function.exif-thumbnail.md: exif\_thumbnail »
  - index.md: PHP Manual
  - ref.exif.md: Exif Функції
title: exif\_tagname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exif\_tagname

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

exif\_tagname — Отримання імені заголовка за його індексом

### Опис

```methodsynopsis
exif_tagname(int $index): string|false
```

### Список параметрів

`index`

ID тега, ім'я якого потрібно отримати.

### Значення, що повертаються

Повертає ім'я заголовка або **`false`**, якщо `index` не є певним ідентифікатором EXIF ​​тега.

### Приклади

**Приклад #1 Приклад використання** exif\_tagname()\*\*\*\*

```php
<?php
echo "256: ".exif_tagname(256).PHP_EOL;
echo "257: ".exif_tagname(257).PHP_EOL;
?>
```

Результат виконання наведеного прикладу:

```
256: ImageWidth
257: ImageLength
```

### Дивіться також

-   [exif\_imagetype()](function.exif-imagetype.md) \- Determine the type of an image
-   [» EXIF специфікація](http://exif.org/Exif2-2.PDF)
-   [» EXIF теги](http://www.sno.phy.queensu.ca/~phil/exiftool/TagNames/EXIF.md)
