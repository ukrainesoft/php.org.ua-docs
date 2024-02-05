---
navigation:
  - function.finfo-close.md: « finfo\_close
  - function.finfo-open.md: finfo\_open »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: finfo\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# finfo\_file

# finfo::file

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfo\_file -- finfo::file — Повертає інформацію про файл

### Опис

Процедурний стиль

```methodsynopsis
finfo_file(    finfo $finfo,    string $filename,    int $flags = FILEINFO_NONE,    ?resource $context = null): string|false
```

Об'єктно-орієнтований стиль

```methodsynopsis
public finfo::file(string $filename, int $flags = FILEINFO_NONE, ?resource $context = null): string|false
```

Функція використовується для отримання інформації про файл.

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfo\_open()](function.finfo-open.md)

`filename`

Назва файлу, що перевіряється.

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`context`

Для описания`contexts`, смотрите[Функції для роботи з потоками](ref.stream.md)

### Значення, що повертаються

Повертає текстовий опис вмісту файлу `filename`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад использования[finfo\_file()](finfo.file.md)**

```php
<?php
$finfo = finfo_open(FILEINFO_MIME_TYPE); // возвращает mime-тип
foreach (glob("*") as $filename) {
    echo finfo_file($finfo, $filename) . "\n";
}
finfo_close($finfo);
?>
```

Висновок наведеного прикладу буде схожим на:

```
text/html
image/gif
application/vnd.ms-excel
```

### Дивіться також

-   [finfo\_buffer()](finfo.buffer.md) \- Псевдонім finfo\_buffer()
