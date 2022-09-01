---
navigation:
  - function.stream-is-local.html: « streamісlocal
  - function.stream-notification-callback.html: streamnotificationcallback »
  - index.html: PHP Manual
  - ref.stream.html: Функції для роботи з потоками
title: streamisatty
---
# streamisatty

(PHP 7> = 7.2.0, PHP 8)

streamisatty — Перевіряє, чи є потік TTY

### Опис

```methodsynopsis
stream_isatty(resource $stream): bool
```

Визначає, чи належить потік `stream` до дійсного пристрою термінального типу Це більш переносима версія [posixisatty()](function.posix-isatty.html)оскільки вона працює і в системах Windows.

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
