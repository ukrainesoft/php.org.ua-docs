Повертає інформацію про файл

-   [« finfoclose](function.finfo-close.html)
    
-   [finfoopen »](function.finfo-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции модуля Fileinfo](ref.fileinfo.html)
    
-   Повертає інформацію про файл
    

# finfofile

# finfo::file

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfofile -- finfo::file — Повертає інформацію про файл

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

Екземпляр [finfo](class.finfo.html), що повертається функцією [finfoopen()](function.finfo-open.html)

`filename`

Назва файлу, що перевіряється.

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.html)

`context`

Для опису `contexts`, дивіться [Функції для роботи з потоками](ref.stream.html)

### Значення, що повертаються

Повертає текстовий опис вмісту файлу `filename` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання [finfofile()](finfo.file.html)**

```php
<?php
$finfo = finfo_open(FILEINFO_MIME_TYPE); // возвращает mime-тип
foreach (glob("*") as $filename) {
    echo finfo_file($finfo, $filename) . "\n";
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

-   [finfobuffer()](finfo.buffer.html) - Псевдонім finfobuffer()