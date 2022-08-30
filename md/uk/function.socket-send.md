Надсилає дані в приєднаний сокет

-   [« socketselect](function.socket-select.html)
    
-   [socketsendmsg »](function.socket-sendmsg.html)
    
-   [PHP Manual](index.md)
    
-   [Функции сокета](ref.sockets.md)
    
-   Надсилає дані в приєднаний сокет
    

# socketsend

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketsend — Надсилає дані в приєднаний сокет

### Опис

```methodsynopsis
socket_send(    Socket $socket,    string $data,    int $length,    int $flags): int|false
```

Функція **socketsend()** відправляє `length` байт у сокет `socket` з буфера `data`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.html) або [socketaccept()](function.socket-accept.html)

`data`

Буфер містить дані, які будуть відправлені на віддалений хост.

`length`

Число байт, яке буде відправлено на віддалений хост з буфера `data`

`flags`

Значення параметру `flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (`|`

<table class="doctable table"><caption><strong>Можливі значення для параметра <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>MSG_OOB</code></strong></td><td>Надіслати дані OOB (out-of-band, позасмугові).</td></tr><tr><td><strong><code>MSG_EOR</code></strong></td><td>Вказує на позначку запису. Надіслані дані завершують запис.</td></tr><tr><td><strong><code>MSG_EOF</code></strong></td><td>Закриває відправну сторону сокету і додає відповідне повідомлення про цьому на кінці даних, що відправляються. Надані дані завершують транзакцію.</td></tr><tr><td><strong><code>MSG_DONTROUTE</code></strong></td><td>Не використовувати роутинг, використовувати прямий інтерфейс.&lt; /td&gt;</td></tr></tbody></table>

### Значення, що повертаються

**socketsend()** повертає кількість відправлених байтів або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                  |
|--------|-------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketsendto()](function.socket-sendto.html) - Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні