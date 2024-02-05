---
navigation:
  - function.socket-sendmsg.md: « socket\_sendmsg
  - function.socket-set-block.md: socket\_set\_block »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_sendto
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_sendto

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_sendto — Надсилає повідомлення до сокету, незалежно від того, приєднаний він чи ні

### Опис

```methodsynopsis
socket_sendto(    Socket $socket,    string $data,    int $length,    int $flags,    string $address,    ?int $port = null): int|false
```

Функция\*\*socket\_sendto()\*\*отправляет`length`байт из буфера`buf`через сокет`socket`к порту`port`на адресе`address`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою [socket\_create()](function.socket-create.md)

`data`

Дані будуть взяті з буфера `data`

`length`

`length`байт из буфера`data`будет отправлено.

`flags`

Значение параметра`flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (

< td>**`MSG_EOR`**

<table class="doctable table"><caption><strong>Можливі значення прапорів <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>MSG_OOB</code></strong></td><td>Надіслати дані OOB (out-of-band, позасмугові).</td></tr><tr><td>Вказує на позначку запису. Надіслані дані завершують запис.</td></tr><tr><td><strong><code>MSG_EOF</code></strong></td><td>Закриває відправну сторону сокету і додає відповідне повідомлення про цьому в кінець даних, що відправляються. Надіслані дані завершують транзакцію.</td></tr><tr><td><strong><code>MSG_DONTROUTE</code></strong></td><td>Не використовувати маршрутизацію, використовувати прямий інтерфейс.&lt; /td&gt;</td></tr></tbody></table>

`address`

IP-адреса віддаленого хоста.

`port`

`port` - Це номер віддаленого порту, яким будуть відправлені дані.

### Значення, що повертаються

Функция**socket\_sendto()** повертає кількість байт, відправлених на віддалений хост, або **`false`**, якщо сталася помилка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
| 8.0.0 | `port` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**socket\_sendto()\*\*\*\*

```php
<?php
    $sock = socket_create(AF_INET, SOCK_DGRAM, SOL_UDP);

    $msg = "Пинг !";
    $len = strlen($msg);

    socket_sendto($sock, $msg, $len, 0, '127.0.0.1', 1223);
    socket_close($sock);
?>
```

### Дивіться також

-   [socket\_send()](function.socket-send.md) \- Надсилає дані в приєднаний сокет
