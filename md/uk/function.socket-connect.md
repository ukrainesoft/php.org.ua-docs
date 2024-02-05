---
navigation:
  - function.socket-cmsg-space.md: « socket\_cmsg\_space
  - function.socket-create-listen.md: socket\_create\_listen »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_connect

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_connect — Починає з'єднання з сокетом

### Опис

```methodsynopsis
socket_connect(Socket $socket, string $address, ?int $port = null): bool
```

Ініціалізує з'єднання з адресою `address`, використовуючи екземпляр [Socket](class.socket.md) `socket`, який має бути екземпляром [Socket](class.socket.md), створеним за допомогою функції [socket\_create()](function.socket-create.md)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою [socket\_create()](function.socket-create.md)

`address`

Параметр`address` може бути IPv4-адресою в записі, розділеною точками (наприклад, `127.0.0.1`), якщо параметр `socket`равен\*\*`AF_INET`**, правильна IPv6-адреса (наприклад, `::1`), якщо включена підтримка IPv6 та параметр `socket`равен**`AF_INET6`\*\* або шлях до файлу доменного сокету Unix, якщо використовується сімейство сокетів **`AF_UNIX`**

`port`

Параметр`port` використовується та обов'язковий тільки в тому випадку, якщо відбувається з'єднання з сокетом **`AF_INET`**или**`AF_INET6`**, і він вказує порт на віддаленому хості, до якого має бути створено з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути потім переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

> **Зауваження** :
> 
> Якщо неблокуючий сокет, то ця функція повертає **`false`** з помилкою `Operation now in progress`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
| 8.0.0 | `port` тепер допускає значення null. |

### Дивіться також

-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
