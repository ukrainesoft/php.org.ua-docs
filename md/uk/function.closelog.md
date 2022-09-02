---
navigation:
  - function.checkdnsrr.md: « checkdnsrr
  - function.dns-check-record.md: dnscheckrecord »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: closelog
---
# closelog

(PHP 4, PHP 5, PHP 7, PHP 8)

closelog — Закриває з'єднання із системним журналом

### Опис

```methodsynopsis
closelog(): bool
```

Функція **closelog()** закриває дескриптор, який використовується для запису до системного журналу. Використання **closelog()** не є обов'язковим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [syslog()](function.syslog.md) - Генерує повідомлення для системного журналу
-   [openlog()](function.openlog.md) - Відкриває підключення до системного журналу
