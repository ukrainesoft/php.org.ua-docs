Надіслати повідомлення

-   [« socket\_send](function.socket-send.html)
    
-   [socket\_sendto »](function.socket-sendto.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Надіслати повідомлення
    

# socketsendmsg

(PHP 5> = 5.5.0, PHP 7, PHP 8)

socketsendmsg — Надіслати повідомлення

### Опис

```methodsynopsis
socket_sendmsg(Socket $socket, array $message, int $flags = 0): int|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`socket`

`message`

`flags`

### Значення, що повертаються

Повертає кількість відправлених байтів або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                    |
|--------|---------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_recvmsg()](function.socket-recvmsg.html) - Прочитати повідомлення
-   [socket\_cmsg\_space()](function.socket-cmsg-space.html) - Обчислити розмір буфера повідомлення