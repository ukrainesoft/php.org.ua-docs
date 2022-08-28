Закриває екземпляр Socket

-   [« socket\_clear\_error](function.socket-clear-error.html)
    
-   [socket\_cmsg\_space »](function.socket-cmsg-space.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Закриває екземпляр Socket
    

# socketclose

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketclose — Закриває екземпляр [Socket](class.socket.html)

### Опис

```methodsynopsis
socket_close(Socket $socket): void
```

Функція **socketclose()** закриває екземпляр [Socket](class.socket.html), вказаний параметром `socket`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html)створений за допомогою функцій [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание                                                                                    |
|--------|---------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету