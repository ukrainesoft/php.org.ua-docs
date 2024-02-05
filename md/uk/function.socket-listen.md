---
navigation:
  - function.socket-last-error.md: « socket\_last\_error
  - function.socket-read.md: socket\_read »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_listen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_listen

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_listen — Прослуховує вхідні з'єднання на сокеті

### Опис

```methodsynopsis
socket_listen(Socket $socket, int $backlog = 0): bool
```

Після того, як сокет `socket` був створений за допомогою функції [socket\_create()](function.socket-create.md)и привязан к имени при помощи функции[socket\_bind()](function.socket-bind.md), йому можна вказати слухати вхідні з'єднання на сокеті `socket`

Функция**socket\_listen()** застосовна тільки до сокетів типу **`SOCK_STREAM`**или**`SOCK_SEQPACKET`**

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)створений за допомогою функцій [socket\_create()](function.socket-create.md) або [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md)

`backlog`

Максимум`backlog` вхідних з'єднань буде поміщено у чергу на обробку. Якщо запит на з'єднання прийде, коли черга заповнена, клієнт може отримати помилку `ECONNREFUSED`, або, якщо базовий протокол дозволяє повторну передачу, запит буде повторено.

> **Зауваження** :
> 
> Максимальное значение параметра`backlog` дуже залежить використовується платформи. У Linux дуже велике значення буде мовчки обрізано до **`SOMAXCONN`**. У win32, якщо передано **`SOMAXCONN`**, базовий провайдер сервісу, відповідального за сокет, встановить цей параметр максимальним *розумним* значенням. Немає стандартного способу дізнатися про актуальне значення "backlog" для цієї платформи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_accept()](function.socket-accept.md) \- приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md) \- Створити та прив'язати до сокету із зазначеного addrinfo
