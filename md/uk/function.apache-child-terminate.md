---
navigation:
  - ref.apache.md: « Функції Apache
  - function.apache-get-modules.md: apache\_get\_modules »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_child\_terminate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_child\_terminate

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

apache\_child\_terminate — Завершити процес Apache після закінчення поточного запиту

### Опис

```methodsynopsis
apache_child_terminate(): void
```

**apache\_child\_terminate()** реєструє процес Apache, що обслуговує поточний запит PHP для того, щоб завершити його після закінчення PHP-скрипту. Ця функція може бути використана для завершення процесу, для роботи якого знадобилася значна кількість оперативної пам'яті, яка не була повернена операційній системі після завершення роботи PHP-скрипту.

Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.

### Дивіться також

-   [exit()](function.exit.md) \- Виводить повідомлення та припиняє виконання поточного скрипту
