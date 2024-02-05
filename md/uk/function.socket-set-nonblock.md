---
navigation:
  - function.socket-set-block.md: « socket\_set\_block
  - function.socket-set-option.md: socket\_set\_option »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_set\_nonblock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_set\_nonblock

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_set\_nonblock — Встановлює неблокуючий режим файлового дескриптора fd

### Опис

```methodsynopsis
socket_set_nonblock(Socket $socket): bool
```

Функция**socket\_set\_nonblock()**устанавливает флаг**`O_NONBLOCK`** на сокеті, вказаному у параметрі `socket`

Коли операція (наприклад, отримання, відправлення, з'єднання, прийняття з'єднання, ...) виконується на неблокуючому сокеті, скрипт не припинятиме своє виконання до отримання сигналу або можливості виконати операцію. Якщо операція, що виконується, повинна привести до блокування виконання скрипта, то замість цього викликана функція поверне помилку.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання** socket\_set\_nonblock()\*\*\*\*

```php
<?php
$socket = socket_create_listen(1223);
socket_set_nonblock($socket);

socket_accept($socket);
?>
```

Цей приклад створює сокет, що слухає, на всіх інтерфейсах на порту 1223 і встановлює сокет в режим **`O_NONBLOCK`**. . [socket\_accept()](function.socket-accept.md) буде негайно повертати помилку, якщо тільки в цей момент немає очікуваного з'єднання.

### Дивіться також

-   [socket\_set\_block()](function.socket-set-block.md) \- Встановлює блокуючий режим на сокеті
-   [socket\_set\_option()](function.socket-set-option.md) \- Встановлює опції для сокету
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
