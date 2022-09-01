---
navigation:
  - function.socket-connect.html: « socketconnect
  - function.socket-create-pair.html: socketcreatepair »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketcreatelisten
---
# socketcreatelisten

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketcreatelisten — Відкриває сокет на вказаному порту для отримання з'єднань

### Опис

```methodsynopsis
socket_create_listen(int $port, int $backlog = 128): Socket|false
```

**socketcreatelisten()** створює новий екземпляр [Socket](class.socket.md) типу \*\*`AF_INET`\*\*слухає на *всіх* локальних інтерфейсів вказаний порт в очікуванні нових з'єднань.

Ця функція призначена для спрощення завдання створення нового сокету, який слухає порт для отримання нових з'єднань.

### Список параметрів

`port`

Порт, який слід слухати на всіх інтерфейсах.

`backlog`

Параметр `backlog` визначає максимальну довжину, до якої може зрости черга з'єднань, що очікують. . **`SOMAXCONN`** може бути переданий як параметр `backlog`, дивіться [socketlisten()](function.socket-listen.md) для повнішої інформації.

### Значення, що повертаються

**socketcreatelisten()** повертає новий екземпляр [Socket](class.socket.md) у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socketlasterror()](function.socket-last-error.html). Цей код може бути переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |

### Примітки

> **Зауваження**
> 
> Якщо ви хочете створити сокет, який прослуховуватиме лише певний інтерфейс, вам потрібно використовувати функції [socketcreate()](function.socket-create.html) [socketbind()](function.socket-bind.html) і [socketlisten()](function.socket-listen.md)

### Дивіться також

-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketcreatepair()](function.socket-create-pair.md) - Створює пару нерозрізнених сокетів та зберігає їх у масиві
-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
