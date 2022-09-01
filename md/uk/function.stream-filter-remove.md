---
navigation:
  - function.stream-filter-register.html: « streamfilterregister
  - function.stream-get-contents.html: streamgetcontents »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamfilterremove
---
# streamfilterremove

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamfilterremove — Видалити фільтр із потоку

### Опис

```methodsynopsis
stream_filter_remove(resource $stream_filter): bool
```

Видаляє потоковий фільтр, раніше доданий до потоку за допомогою функції [streamfilterprepend()](function.stream-filter-prepend.html) або [streamfilterappend()](function.stream-filter-append.md). Будь-які дані, що залишилися у внутрішньому буфері фільтра, будуть відправлені до наступного фільтра до його видалення.

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

-   [streamfilterregister()](function.stream-filter-register.md) - Реєструє потоковий фільтр, визначений користувачем
-   [streamfilterappend()](function.stream-filter-append.md) - Прикріпити фільтр до потоку
-   [streamfilterprepend()](function.stream-filter-prepend.md) - Прикріплює фільтр до потоку
