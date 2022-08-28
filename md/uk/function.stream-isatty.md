Перевіряє, чи є потік TTY

-   [« stream\_is\_local](function.stream-is-local.html)
    
-   [stream\_notification\_callback »](function.stream-notification-callback.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Перевіряє, чи є потік TTY
    

# streamisatty

(PHP 7> = 7.2.0, PHP 8)

streamisatty — Перевіряє, чи є потік TTY

### Опис

```methodsynopsis
stream_isatty(resource $stream): bool
```

Визначає, чи належить потік `stream` до дійсного пристрою термінального типу Це більш переносима версія [posix\_isatty()](function.posix-isatty.html)оскільки вона працює і в системах Windows.

### Список параметрів

`stream`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад виконання **streamisatty()****

Ця команда може використовуватися для визначення, чи перенаправлений стандартний потік даних / стандартний потік помилок у файл.

php -r "varexport(stream)isatty(STDERR));"

Результатом виконання цього прикладу буде щось подібне:

true

php -r "varexport(stream)isatty(STDERR));" 2>output.txt

Результатом виконання цього прикладу буде щось подібне:

false