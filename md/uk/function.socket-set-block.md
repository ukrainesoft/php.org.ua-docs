---
navigation:
  - function.socket-sendto.md: « socket\_sendto
  - function.socket-set-nonblock.md: socket\_set\_nonblock »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_set\_block
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_set\_block

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

socket\_set\_block — Встановлює блокуючий режим на сокеті

### Опис

```methodsynopsis
socket_set_block(Socket $socket): bool
```

Функция**socket\_set\_block()** прибирає прапор **`O_NONBLOCK`** із сокету, вказаного у параметрі `socket`

Коли операція (наприклад, отримання, відправлення, з'єднання, прийняття з'єднання, ...) виконується на блокувальному сокеті, скрипт припинятиме своє виконання доти, доки він не отримає сигнал або можливість виконати операцію.

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

**Приклад #1 Приклад використання**socket\_set\_block()\*\*\*\*

```php
<?php
$socket = socket_create_listen(1223);
socket_set_block($socket);

socket_accept($socket);
?>
```

Цей приклад створює сокет, що слухає, на всіх інтерфейсах на порту 1223 і встановлює сокет в режим \*\*`O_BLOCK`\*\*Функция[socket\_accept()](function.socket-accept.md)зависнет до тех пор, пока не будет принято соединение.

### Дивіться також

-   [socket\_set\_nonblock()](function.socket-set-nonblock.md) \- Встановлює неблокуючий режим файлового дескриптора fd
-   [socket\_set\_option()](function.socket-set-option.md) \- Встановлює опції для сокету
