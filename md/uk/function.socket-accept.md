---
navigation:
  - ref.sockets.md: « Функции сокета
  - function.socket-addrinfo-bind.md: socketaddrinfobind »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketaccept
---
# socketaccept

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketaccept — Приймає з'єднання на сокеті

### Опис

```methodsynopsis
socket_accept(Socket $socket): Socket|false
```

Після того, як сокет `socket` був створений за допомогою функції [socketcreate()](function.socket-create.md), прив'язаний до імені за допомогою функції [socketbind()](function.socket-bind.md), і йому було вказано слухати з'єднання за допомогою функції [socketlisten()](function.socket-listen.md), ця функція прийматиме вхідні з'єднання на цьому сокеті. Як тільки відбулося вдале з'єднання, повертається екземпляр [Socket](class.socket.md)який може бути використаний для зв'язку. Якщо у черзі сокету є кілька з'єднань, буде використано перше з них. Якщо немає з'єднань, що очікують, то функція **socketaccept()** буде блокувати виконання скрипту доти, доки з'явиться з'єднання. Якщо сокет `socket` був зроблений неблокуючим за допомогою функції [socketsetblocking()](function.socket-set-blocking.md) або [socketsetnonblock()](function.socket-set-nonblock.md), буде повернуто **`false`**

Екземпляр [Socket](class.socket.md)отриманий за допомогою функції **socketaccept()** не може бути використаний для прийняття нових з'єднань. Проте початковий сокет, що слухає `socket`, залишається відкритим та може бути використаний повторно.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md)

### Значення, що повертаються

У разі успішного виконання повертає екземпляр [Socket](class.socket.md) або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою виклику функції [socketlasterror()](function.socket-last-error.md). Цей код помилки може бути переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [socketconnect()](function.socket-connect.md) - Починає з'єднання із сокетом
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
