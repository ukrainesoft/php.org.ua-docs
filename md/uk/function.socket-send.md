---
navigation:
  - function.socket-select.md: « socket\_select
  - function.socket-sendmsg.md: socket\_sendmsg »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_send
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_send

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_send — Надсилає дані в приєднаний сокет

### Опис

```methodsynopsis
socket_send(    Socket $socket,    string $data,    int $length,    int $flags): int|false
```

Функция\*\*socket\_send()\*\*отправляет`length`байт в сокет`socket`из буфера`data`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

`data`

Буфер містить дані, які будуть відправлені на віддалений хост.

`length`

Число байт, яке буде відправлено на віддалений хост з буфера `data`

`flags`

Значение параметра`flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (

<table class="doctable table"><caption><strong>Можливі значення для параметра <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>MSG_OOB</code></strong></td><td>Надіслати дані OOB (out-of-band, позасмугові).</td></tr><tr><td><strong><code>MSG_EOR</code></strong></td><td>Вказує на позначку запису. Надіслані дані завершують запис.</td></tr><tr><td><strong><code>MSG_EOF</code></strong></td><td>Закриває відправну сторону сокету і додає відповідне повідомлення про цьому на кінці даних, що відправляються. Надані дані завершують транзакцію.</td></tr><tr><td><strong><code>MSG_DONTROUTE</code></strong></td><td>Не використовувати роутинг, використовувати прямий інтерфейс.&lt; /td&gt;</td></tr></tbody></table>

### Значення, що повертаються

**socket\_send()** повертає кількість відправлених байтів або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_sendto()](function.socket-sendto.md) \- Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
