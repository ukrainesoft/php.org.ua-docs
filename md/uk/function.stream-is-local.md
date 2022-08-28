Перевіряє, чи є потік локальним потоком

-   [« stream\_get\_wrappers](function.stream-get-wrappers.html)
    
-   [stream\_isatty »](function.stream-isatty.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Перевіряє, чи є потік локальним потоком
    

# streamісlocal

(PHP 5> = 5.2.4, PHP 7, PHP 8)

streamісlocal — Перевіряє, чи потік є локальним потоком.

### Опис

```methodsynopsis
stream_is_local(resource|string $stream): bool
```

Перевіряє, чи потік або URL локальний чи ні.

### Список параметрів

`stream`

Ресурс потоку або URL для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад виконання**streamісlocal()\*\*\*\*

Приклад простого використання.

```php
<?php
var_dump(stream_is_local("http://example.com"));
var_dump(stream_is_local("/etc"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```