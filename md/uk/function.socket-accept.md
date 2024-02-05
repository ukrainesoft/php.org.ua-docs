---
navigation:
  - ref.sockets.md: « Функції сокету
  - function.socket-addrinfo-bind.md: socket\_addrinfo\_bind »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_accept
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_accept

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_accept — Приймає з'єднання на сокеті

### Опис

```methodsynopsis
socket_accept(Socket $socket): Socket|false
```

Після того, як сокет `socket` був створений за допомогою функції [socket\_create()](function.socket-create.md), привязан к имени при помощи функции[socket\_bind()](function.socket-bind.md), і йому було вказано слухати з'єднання за допомогою функції [socket\_listen()](function.socket-listen.md), ця функція прийматиме вхідні з'єднання на цьому сокеті. Як тільки відбулося вдале з'єднання, повертається екземпляр [Socket](class.socket.md)який може бути використаний для зв'язку. Якщо у черзі сокету є кілька з'єднань, буде використано перше з них. Якщо немає з'єднань, що очікують, то функція **socket\_accept()** буде блокувати виконання скрипту доти, доки з'явиться з'єднання. Якщо сокет `socket` був зроблений неблокуючим за допомогою функції [socket\_set\_blocking()](function.socket-set-blocking.md) або [socket\_set\_nonblock()](function.socket-set-nonblock.md), буде повернуто **`false`**

Екземпляр [Socket](class.socket.md)отриманий за допомогою функції **socket\_accept()** не може бути використаний для прийняття нових з'єднань. Однак початковий сокет, що слухає `socket`, залишається відкритим та може бути використаний повторно.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md)

### Значення, що повертаються

У разі успішного виконання повертає екземпляр [Socket](class.socket.md)или\*\*`false`\*\* у разі виникнення помилки. Код помилки можна отримати за допомогою виклику функції [socket\_last\_error()](function.socket-last-error.md). Цей код помилки може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Дивіться також

-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
