---
navigation:
  - ref.fileinfo.md: « Функції модуля Fileinfo
  - function.finfo-close.md: finfo\_close »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: finfo\_buffer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# finfo\_buffer

# finfo::buffer

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfo\_buffer -- finfo::buffer — Повертає інформацію про рядок буфера

### Опис

Процедурний стиль

```methodsynopsis
finfo_buffer(    finfo $finfo,    string $string,    int $flags = FILEINFO_NONE,    ?resource $context = null): string|false
```

Об'єктно-орієнтований стиль

```methodsynopsis
public finfo::buffer(string $string, int $flags = FILEINFO_NONE, ?resource $context = null): string|false
```

Ця функція використовується для отримання інформації про бінарних даних у рядку.

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfo\_open()](function.finfo-open.md)

`string`

Вміст файлу, що перевіряється.

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`context`

### Значення, що повертаються

Повертає текстовий опис для аргументу `string`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад[finfo\_buffer()](finfo.buffer.md)**

```php
<?php
$finfo = new finfo(FILEINFO_MIME);
echo $finfo->buffer($_POST["script"]) . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
application/x-sh; charset=us-ascii
```

### Дивіться також

-   [finfo\_file()](finfo.file.md) \- Псевдонім finfo\_file()
