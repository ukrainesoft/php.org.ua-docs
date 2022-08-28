Приймає з'єднання на сокеті

-   [« Функции сокета](ref.sockets.html)
    
-   [socket\_addrinfo\_bind »](function.socket-addrinfo-bind.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Приймає з'єднання на сокеті
    

# socketaccept

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketaccept — Приймає з'єднання на сокеті

### Опис

```methodsynopsis
socket_accept(Socket $socket): Socket|false
```

Після того, як сокет `socket` був створений за допомогою функції [socket\_create()](function.socket-create.html), прив'язаний до імені за допомогою функції [socket\_bind()](function.socket-bind.html), і йому було вказано слухати з'єднання за допомогою функції [socket\_listen()](function.socket-listen.html), ця функція прийматиме вхідні з'єднання на цьому сокеті. Як тільки відбулося вдале з'єднання, повертається екземпляр [Socket](class.socket.html)який може бути використаний для зв'язку. Якщо у черзі сокету є кілька з'єднань, буде використано перше з них. Якщо немає з'єднань, що очікують, то функція **socketaccept()** буде блокувати виконання скрипту доти, доки з'явиться з'єднання. Якщо сокет `socket` був зроблений неблокуючим за допомогою функції [socket\_set\_blocking()](function.socket-set-blocking.html) або [socket\_set\_nonblock()](function.socket-set-nonblock.html), буде повернуто **`false`**

Екземпляр [Socket](class.socket.html)отриманий за допомогою функції **socketaccept()** не може бути використаний для прийняття нових з'єднань. Проте початковий сокет, що слухає `socket`, залишається відкритим та може бути використаний повторно.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socket\_create()](function.socket-create.html)

### Значення, що повертаються

У разі успішного виконання повертає екземпляр [Socket](class.socket.html) або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою виклику функції [socket\_last\_error()](function.socket-last-error.html). Цей код помилки може бути переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.html); раніше повертався ресурс (resource). |

### Дивіться також

-   [socket\_connect()](function.socket-connect.html) - Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету