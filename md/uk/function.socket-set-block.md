---
navigation:
  - function.socket-sendto.html: « socketsendto
  - function.socket-set-nonblock.html: socketsetnonblock »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketsetblock
---
# socketsetblock

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

socketsetblock — Встановлює блокуючий режим на сокеті

### Опис

```methodsynopsis
socket_set_block(Socket $socket): bool
```

Функція **socketsetblock()** прибирає прапор **`O_NONBLOCK`** із сокету, вказаного у параметрі `socket`

Коли операція (наприклад, отримання, відправлення, з'єднання, прийняття з'єднання, ...) виконується на блокувальному сокеті, скрипт буде припиняти своє виконання доти, доки він не отримає сигнал або можливість виконати операцію.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socketcreate()](function.socket-create.html) або [socketaccept()](function.socket-accept.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання**socketsetblock()\*\*\*\*

```php
<?php
$socket = socket_create_listen(1223);
socket_set_block($socket);

socket_accept($socket);
?>
```

Цей приклад створює сокет, що слухає, на всіх інтерфейсах на порту 1223 і встановлює сокет в режим **`O_BLOCK`**. Функція [socketaccept()](function.socket-accept.html) зависне доти, доки не буде прийнято з'єднання.

### Дивіться також

-   [socketsetnonblock()](function.socket-set-nonblock.html) - Встановлює неблокуючий режим файлового дескриптора fd
-   [socketsetoption()](function.socket-set-option.html) - Встановлює опції для сокету
