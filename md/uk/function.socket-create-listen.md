---
navigation:
  - function.socket-connect.md: « socket\_connect
  - function.socket-create-pair.md: socket\_create\_pair »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_create\_listen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_create\_listen

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_create\_listen — Відкриває сокет на вказаному порту для отримання з'єднань

### Опис

```methodsynopsis
socket_create_listen(int $port, int $backlog = 128): Socket|false
```

**socket\_create\_listen()** створює новий екземпляр [Socket](class.socket.md)типа\*\*`AF_INET`\*\*, слушающий на*всіх* локальних інтерфейсів вказаний порт в очікуванні нових з'єднань.

Ця функція призначена для спрощення завдання створення нового сокету, який слухає порт для отримання нових з'єднань.

### Список параметрів

`port`

Порт, який слід слухати на всіх інтерфейсах.

`backlog`

Параметр`backlog` визначає максимальну довжину, до якої може зрости черга з'єднань, що очікують. . **`SOMAXCONN`** може бути переданий як параметр `backlog`, смотрите[socket\_listen()](function.socket-listen.md) для повнішої інформації.

### Значення, що повертаються

**socket\_create\_listen()** повертає новий екземпляр [Socket](class.socket.md) у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Примітки

> **Зауваження** :
> 
> Якщо ви хочете створити сокет, який прослуховуватиме лише певний інтерфейс, вам потрібно використовувати функції [socket\_create()](function.socket-create.md) [socket\_bind()](function.socket-bind.md) і [socket\_listen()](function.socket-listen.md)

### Дивіться також

-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_create\_pair()](function.socket-create-pair.md) \- Створює пару нерозрізнених сокетів та зберігає їх у масиві
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
