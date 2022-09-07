---
navigation:
  - function.finfo-close.md: « finfoclose
  - function.finfo-open.md: finfoopen »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функции модуля Fileinfo
title: finfofile
---
# finfofile

# finfo::file

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfofile -- finfo::file — Повертає інформацію про файл

### Опис

Процедурний стиль

```methodsynopsis
finfo_file(    finfo $finfo,    string $filename,    int $flags = FILEINFO_NONE,    ?resource $context = null): string|false
```

Об'єктно-орієнтований стиль

```methodsynopsis
public finfo::file(string $filename, int $flags = FILEINFO_NONE, ?resource $context = null): string|false
```

Функція використовується для отримання інформації про файл.

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfoopen()](function.finfo-open.md)

`filename`

Назва файлу, що перевіряється.

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`context`

Для опису `contexts`, дивіться [Функції для роботи з потоками](ref.stream.md)

### Значення, що повертаються

Повертає текстовий опис вмісту файлу `filename` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання [finfofile()](finfo.file.md)**

```php
<?php
$finfo = finfo_open(FILEINFO_MIME_TYPE); // возвращает mime-тип
foreach (glob("*") as $filename) {
    echo finfo_file($finfo, $filename) . "\n";
}
finfo_close($finfo);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
text/html
image/gif
application/vnd.ms-excel
```

### Дивіться також

-   [finfobuffer()](finfo.buffer.md) - Псевдонім finfobuffer()
