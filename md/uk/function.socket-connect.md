---
navigation:
  - function.socket-cmsg-space.md: « socketcmsgspace
  - function.socket-create-listen.md: socketcreatelisten »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketconnect
---
# socketconnect

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketconnect — Починає з'єднання з сокетом

### Опис

```methodsynopsis
socket_connect(Socket $socket, string $address, ?int $port = null): bool
```

Ініціалізує з'єднання з адресою `address`, використовуючи екземпляр [Socket](class.socket.md) `socket`, який має бути екземпляром [Socket](class.socket.md), створеним за допомогою функції [socketcreate()](function.socket-create.md)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою [socketcreate()](function.socket-create.md)

`address`

Параметр `address` може бути IPv4-адресою в записі, розділеною точками (наприклад, `127.0.0.1`), якщо параметр `socket` дорівнює **`AF_INET`**, правильна IPv6-адреса (наприклад, `::1`), якщо включена підтримка IPv6 та параметр `socket` дорівнює **`AF_INET6`** або шлях до файлу доменного сокету Unix, якщо використовується сімейство сокетів **`AF_UNIX`**

`port`

Параметр `port` використовується та обов'язковий тільки в тому випадку, якщо відбувається з'єднання з сокетом **`AF_INET`** або **`AF_INET6`**, і він вказує порт на віддаленому хості, до якого має бути створено з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socketlasterror()](function.socket-last-error.md). Цей код може бути потім переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

> **Зауваження**
> 
> Якщо неблокуючий сокет, то ця функція повертає **`false`** з помилкою `Operation now in progress`

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
|  | `port` тепер допускає значення null. |

### Дивіться також

-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
