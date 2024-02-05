---
navigation:
  - function.checkdnsrr.md: « checkdnsrr
  - function.dns-check-record.md: dns\_check\_record »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: closelog
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# closelog

(PHP 4, PHP 5, PHP 7, PHP 8)

closelog — Закриває з'єднання із системним журналом

### Опис

```methodsynopsis
closelog(): true
```

Функция**closelog()** закриває дескриптор, який використовується для запису до системного журналу. Використання **closelog()** не є обов'язковим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [syslog()](function.syslog.md) \- Генерує повідомлення для системного журналу
-   [openlog()](function.openlog.md) \- Відкриває підключення до системного журналу
