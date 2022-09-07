---
navigation:
  - function.socket-set-block.md: « socketsetblock
  - function.socket-set-option.md: socketsetoption »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketsetnonblock
---
# socketsetnonblock

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketsetnonblock — Встановлює неблокуючий режим файлового дескриптора fd

### Опис

```methodsynopsis
socket_set_nonblock(Socket $socket): bool
```

Функція **socketsetnonblock()** встановлює прапор **`O_NONBLOCK`** на сокеті, вказаному у параметрі `socket`

Коли операція (наприклад, отримання, відправлення, з'єднання, прийняття з'єднання, ...) виконується на неблокуючому сокеті, скрипт не припинятиме своє виконання до отримання сигналу або можливості виконати операцію. Якщо операція, що виконується, повинна привести до блокування виконання скрипта, то замість цього викликана функція поверне помилку.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md) або [socketaccept()](function.socket-accept.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання **socketsetnonblock()****

```php
<?php
$socket = socket_create_listen(1223);
socket_set_nonblock($socket);

socket_accept($socket);
?>
```

Цей приклад створює сокет, що слухає, на всіх інтерфейсах на порту 1223 і встановлює сокет в режим **`O_NONBLOCK`**. . [socketaccept()](function.socket-accept.md) буде негайно повертати помилку, якщо тільки в цей момент немає очікуваного з'єднання.

### Дивіться також

-   [socketsetblock()](function.socket-set-block.md) - Встановлює блокуючий режим на сокеті
-   [socketsetoption()](function.socket-set-option.md) - Встановлює опції для сокету
-   [streamsetblocking()](function.stream-set-blocking.md) - Встановити блокуючий/неблокуючий режим у потоці
