---
navigation:
  - function.socket-last-error.md: « socketlasterror
  - function.socket-read.md: socketread »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketlisten
---
# socketlisten

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketlisten — Прослуховує вхідні з'єднання на сокеті

### Опис

```methodsynopsis
socket_listen(Socket $socket, int $backlog = 0): bool
```

Після того, як сокет `socket` був створений за допомогою функції [socketcreate()](function.socket-create.md) та прив'язаний до імені за допомогою функції [socketbind()](function.socket-bind.md), йому можна вказати слухати вхідні з'єднання на сокеті `socket`

Функція **socketlisten()** застосовна тільки до сокетів типу **`SOCK_STREAM`** або **`SOCK_SEQPACKET`**

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)створений за допомогою функцій [socketcreate()](function.socket-create.md) або [socketaddrinfobind()](function.socket-addrinfo-bind.md)

`backlog`

Максимум `backlog` вхідних з'єднань буде поміщено у чергу на обробку. Якщо запит на з'єднання прийде, коли черга заповнена, клієнт може отримати помилку `ECONNREFUSED`, або, якщо базовий протокол дозволяє повторну передачу, запит буде повторено.

> **Зауваження**
> 
> Максимальне значення параметра `backlog` дуже залежить використовується платформи. У Linux дуже велике значення буде мовчки обрізано до **`SOMAXCONN`**. У win32, якщо передано **`SOMAXCONN`**, базовий провайдер сервісу, відповідального за сокет, встановить цей параметр максимальним *розумним* значенням. Немає стандартного способу дізнатися про актуальне значення "backlog" для цієї платформи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки може бути отриманий за допомогою функції [socketlasterror()](function.socket-last-error.md). Цей код може бути переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketaccept()](function.socket-accept.md) - приймає з'єднання на сокеті
-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketconnect()](function.socket-connect.md) - Починає з'єднання із сокетом
-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
-   [socketaddrinfobind()](function.socket-addrinfo-bind.md) - Створити та прив'язати до сокету із зазначеного addrinfo
