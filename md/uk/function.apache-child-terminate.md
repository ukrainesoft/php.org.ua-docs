---
navigation:
  - ref.apache.html: « Функции Apache
  - function.apache-get-modules.html: apachegetmodules »
  - index.html: PHP Manual
  - ref.apache.html: Функции Apache
title: apachechildterminate
---
# apachechildterminate

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

apachechildterminate — Завершити процес Apache після закінчення поточного запиту

### Опис

```methodsynopsis
apache_child_terminate(): void
```

**apachechildterminate()** реєструє процес Apache, що обслуговує поточний запит PHP для того, щоб завершити його після закінчення PHP-скрипту. Ця функція може бути використана для завершення процесу, для роботи якого знадобилася значна кількість оперативної пам'яті, яка не була повернена операційній системі після завершення роботи PHP-скрипту.

Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.

### Дивіться також

-   [exit()](function.exit.md) - Вивести повідомлення та припинити виконання поточного скрипту
