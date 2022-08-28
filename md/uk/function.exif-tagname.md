Отримання імені заголовка за його індексом

-   [« exif\_read\_data](function.exif-read-data.html)
    
-   [exif\_thumbnail »](function.exif-thumbnail.html)
    
-   [PHP Manual](index.html)
    
-   [Exif Функции](ref.exif.html)
    
-   Отримання імені заголовка за його індексом
    

# exiftagname

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

exiftagname — Отримання імені заголовка за його індексом

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

**Приклад #1 Приклад використання **exiftagname()****

```php
<?php
echo "256: ".exif_tagname(256).PHP_EOL;
echo "257: ".exif_tagname(257).PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
256: ImageWidth
257: ImageLength
```

### Дивіться також

-   [exif\_imagetype()](function.exif-imagetype.html) - Визначте тип зображення.
-   [» EXIF спецификация](http://exif.org/Exif2-2.PDF)
-   [» EXIF теги](http://www.sno.phy.queensu.ca/~phil/exiftool/TagNames/EXIF.html)