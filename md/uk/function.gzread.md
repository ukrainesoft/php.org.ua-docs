---
navigation:
  - function.gzputs.md: « gzputs
  - function.gzrewind.md: gzrewind »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzread
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzread

(PHP 4, PHP 5, PHP 7, PHP 8)

gzread — Бінарне читання gz-файлу

### Опис

```methodsynopsis
gzread(resource $stream, int $length): string|false
```

**gzread()** читає (розпаковуючи) до `length` байт із gz-файлу з переданого покажчика gz-файлу. Читання закінчується при досягненні максимального розміру `length` розпакованих даних або кінця файлу (EOF)

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

`length`

Кількість байт (після розпакування), які слід прочитати.

### Значення, що повертаються

Прочитані дані або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | У разі виникнення помилки повертається **`false`**; раніше, повертався |

### Приклади

**Пример #1 Пример использования**gzread()\*\*\*\*

```php
<?php
// поместить содержимое gz-файла в строку
$filename = "/usr/local/something.txt.gz";
$zd = gzopen($filename, "r");
$contents = gzread($zd, 10000);
gzclose($zd);
?>
```

### Дивіться також

-   [gzwrite()](function.gzwrite.md) \- Бінарний запис у gz-файл
-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
-   [gzgets()](function.gzgets.md) \- Отримати рядок із покажчика файлу
-   [gzgetss()](function.gzgetss.md) \- Повертає рядок із покажчика gz-файлу та видалити HTML-теги
-   [gzfile()](function.gzfile.md) \- Зчитує весь gz-файл у масив
-   [gzpassthru()](function.gzpassthru.md) \- Виведення всіх даних з покажчика gz-файлу.
