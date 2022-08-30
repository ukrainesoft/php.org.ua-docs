Отримати список зареєстрованих транспортів сокету

-   [« streamgetmetadata](function.stream-get-meta-data.html)
    
-   [streamgetwrappers »](function.stream-get-wrappers.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Отримати список зареєстрованих транспортів сокету
    

# streamgettransports

(PHP 5, PHP 7, PHP 8)

streamgettransports — Отримати список зареєстрованих транспортів сокету

### Опис

```methodsynopsis
stream_get_transports(): array
```

Повертає індексований масив, який містить назви всіх транспортів сокету, доступних на запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив назв транспорту сокету.

### Приклади

**Приклад #1 Приклад використання **streamgettransports()****

```php
<?php
$xportlist = stream_get_transports();
print_r($xportlist);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array (
  [0] => tcp
  [1] => udp
  [2] => unix
  [3] => udg
)
```

### Дивіться також

-   [streamgetfilters()](function.stream-get-filters.html) - Отримати список зареєстрованих фільтрів
-   [streamgetwrappers()](function.stream-get-wrappers.html) - Отримати список зареєстрованих потоків