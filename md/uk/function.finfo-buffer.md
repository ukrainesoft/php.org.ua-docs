Повертає інформацію про рядок буфера

-   [« Функции модуля Fileinfo](ref.fileinfo.md)
    
-   [finfoclose »](function.finfo-close.html)
    
-   [PHP Manual](index.md)
    
-   [Функции модуля Fileinfo](ref.fileinfo.md)
    
-   Повертає інформацію про рядок буфера
    

# finfobuffer

# finfo::buffer

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfobuffer -- finfo::buffer — Повертає інформацію про рядок буфера

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

Екземпляр [finfo](class.finfo.md), що повертається функцією [finfoopen()](function.finfo-open.html)

`string`

Вміст файлу, що перевіряється.

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`context`

### Значення, що повертаються

Повертає текстовий опис для аргументу `string` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                         |
|--------|----------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|        | `context` тепер допускає значення null.                                                                                          |

### Приклади

**Приклад #1 Приклад [finfobuffer()](finfo.buffer.md)**

```php
<?php
$finfo = new finfo(FILEINFO_MIME);
echo $finfo->buffer($_POST["script"]) . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
application/x-sh; charset=us-ascii
```

### Дивіться також

-   [finfofile()](finfo.file.md) - Псевдонім finfofile()