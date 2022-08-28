Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні

-   [« socket\_sendmsg](function.socket-sendmsg.html)
    
-   [socket\_set\_block »](function.socket-set-block.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
    

# socketsendto

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketsendto — Надсилає повідомлення до сокету, незалежно від того, приєднаний він чи ні

### Опис

```methodsynopsis
socket_sendto(    Socket $socket,    string $data,    int $length,    int $flags,    string $address,    ?int $port = null): int|false
```

Функція **socketsendto()** відправляє `length` байт із буфера `buf` через сокет `socket` до порту `port` на адресі `address`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою [socket\_create()](function.socket-create.html)

`data`

Дані будуть взяті з буфера `data`

`length`

`length` байт із буфера `data` буде надіслано.

`flags`

Значення параметру `flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (`|`

< td>**`MSG_EOR`**

<table class="doctable table"><caption><strong>Можливі значення прапорів <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>MSG_OOB</code></strong></td><td>Надіслати дані OOB (out-of-band, позасмугові).</td></tr><tr><td>Вказує на позначку запису. Надіслані дані завершують запис.</td></tr><tr><td><strong><code>MSG_EOF</code></strong></td><td>Закриває відправну сторону сокету і додає відповідне повідомлення про цьому в кінець даних, що відправляються. Надіслані дані завершують транзакцію.</td></tr><tr><td><strong><code>MSG_DONTROUTE</code></strong></td><td>Не використовувати маршрутизацію, використовувати прямий інтерфейс.</td><td>/td&gt;</td></tr></tbody></table>

`address`

IP-адреса віддаленого хоста.

`port`

`port` - Це номер віддаленого порту, яким будуть відправлені дані.

### Значення, що повертаються

Функція **socketsendto()** повертає кількість байт, відправлених на віддалений хост, або **`false`**, якщо сталася помилка.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |
|  | `port` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **socketsendto()****

```php
<?php
    $sock = socket_create(AF_INET, SOCK_DGRAM, SOL_UDP);

    $msg = "Пинг !";
    $len = strlen($msg);

    socket_sendto($sock, $msg, $len, 0, '127.0.0.1', 1223);
    socket_close($sock);
?>
```

### Дивіться також

-   [socket\_send()](function.socket-send.html) - Надсилає дані в приєднаний сокет