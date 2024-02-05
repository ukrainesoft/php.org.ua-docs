---
navigation:
  - function.stream-is-local.md: « stream\_is\_local
  - function.stream-notification-callback.md: stream\_notification\_callback »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_isatty
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_isatty

(PHP 7 >= 7.2.0, PHP 8)

stream\_isatty — Перевіряє, чи є потік TTY

### Опис

```methodsynopsis
stream_isatty(resource $stream): bool
```

Визначає, чи належить потік `stream` до дійсного пристрою термінального типу Це більш переносима версія [posix\_isatty()](function.posix-isatty.md)оскільки вона працює і в системах Windows.

### Список параметрів

`stream`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад виконання **stream\_isatty()****

Ця команда може використовуватися для визначення того, чи перенаправлено стандартний потік даних / стандартний потік помилок у файл.

php -r "var\_export(stream\_isatty(STDERR));"

Висновок наведеного прикладу буде схожим на:

true

php -r "var\_export(stream\_isatty(STDERR));" 2>output.txt

Висновок наведеного прикладу буде схожим на:

false
