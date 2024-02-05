---
navigation:
  - function.stream-filter-register.md: « stream\_filter\_register
  - function.stream-get-contents.md: stream\_get\_contents »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_filter\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_filter\_remove

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_filter\_remove — Видалити фільтр із потоку

### Опис

```methodsynopsis
stream_filter_remove(resource $stream_filter): bool
```

Видаляє потоковий фільтр, раніше доданий до потоку за допомогою функції [stream\_filter\_prepend()](function.stream-filter-prepend.md) або [stream\_filter\_append()](function.stream-filter-append.md). Будь-які дані, що залишилися у внутрішньому буфері фільтра, будуть відправлені до наступного фільтра до його видалення.

### Список параметрів

`stream_filter`

Поточний фільтр видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Динамічна зміна фільтрів потоку**

```php
<?php
/* Открытие тестового файла для чтения и записи */
$fp = fopen("test.txt", "rw");

$rot13_filter = stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);
fwrite($fp, "This is ");
stream_filter_remove($rot13_filter);
fwrite($fp, "a test\n");

rewind($fp);
fpassthru($fp);
fclose($fp);

?>
```

Результат виконання наведеного прикладу:

```
Guvf vf a test
```

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.md) \- Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_append()](function.stream-filter-append.md) \- Прикріпити фільтр до потоку
-   [stream\_filter\_prepend()](function.stream-filter-prepend.md) \- Прикріплює фільтр до потоку
