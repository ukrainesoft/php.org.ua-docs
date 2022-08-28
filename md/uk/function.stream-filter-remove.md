Видалити фільтр із потоку

-   [« stream\_filter\_register](function.stream-filter-register.html)
    
-   [stream\_get\_contents »](function.stream-get-contents.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Видалити фільтр із потоку
    

# streamfilterremove

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamfilterremove — Видалити фільтр із потоку

### Опис

```methodsynopsis
stream_filter_remove(resource $stream_filter): bool
```

Видаляє потоковий фільтр, раніше доданий до потоку за допомогою функції [stream\_filter\_prepend()](function.stream-filter-prepend.html) або [stream\_filter\_append()](function.stream-filter-append.html). Будь-які дані, що залишилися у внутрішньому буфері фільтра, будуть відправлені до наступного фільтра до його видалення.

### Список параметрів

`stream_filter`

Поточний фільтр видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Динамічна зміна фільтрів потоку**

```php
<?php
/* Открытие тестового файла для чтения и записи */
$fp = fopen("test.txt", "rw");

$rot13_filter = stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);
fwrite($fp, "This is ");
stream_filter_remove($rot13_filter);
fwrite($fp, "a test\n");

rewind($fp);
fpassthru($fp);
fclose($fp);

?>
```

Результат виконання цього прикладу:

```
Guvf vf a test
```

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.html) - Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_append()](function.stream-filter-append.html) - Прикріпити фільтр до потоку
-   [stream\_filter\_prepend()](function.stream-filter-prepend.html) - Прикріплює фільтр до потоку