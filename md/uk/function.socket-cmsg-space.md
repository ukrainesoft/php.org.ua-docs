Обчислити розмір буфера повідомлення

-   [« socket\_close](function.socket-close.html)
    
-   [socket\_connect »](function.socket-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Обчислити розмір буфера повідомлення
    

# socketcmsgspace

(PHP 5> = 5.5.0, PHP 7, PHP 8)

socketcmsgspace — Визначити розмір буфера повідомлення

### Опис

```methodsynopsis
socket_cmsg_space(int $level, int $type, int $num = 0): ?int
```

Обчислює розмір буфера, який має бути виділено для отримання допоміжних даних.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`level`

`type`

### Значення, що повертаються

### Дивіться також

-   [socket\_recvmsg()](function.socket-recvmsg.html) - Прочитати повідомлення
-   [socket\_sendmsg()](function.socket-sendmsg.html) - Надіслати повідомлення