---
navigation:
  - function.socket-addrinfo-lookup.md: « socket\_addrinfo\_lookup
  - function.socket-bind.md: socket\_bind »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_atmark
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_atmark

(PHP 8 >= 8.3.0, PHP 8)

socket\_atmark — Визначає, чи знаходиться сокет на позасмуговій позначці

### Опис

```methodsynopsis
socket_atmark(Socket $socket): bool
```

Визначає, чи перебуває `socket` на позасмуговій позначці.

### Список параметрів

`socket`

Екземпляр класу [Socket](class.socket.md), створений функцією [socket\_create()](function.socket-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання функції** socket\_atmark()**для установки адреса отправителя**

```php
<?php

// Создать новый сокет
$sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
var_dump(socket_atmark($sock));
// Закрыть сокет
socket_close($sock);
?>
```

### Дивіться також

-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
