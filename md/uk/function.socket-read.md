---
navigation:
  - function.socket-listen.md: « socket\_listen
  - function.socket-recv.md: socket\_recv »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_read

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_read — Читає рядок максимальну довжину байт із сокету

### Опис

```methodsynopsis
socket_read(Socket $socket, int $length, int $mode = PHP_BINARY_READ): string|false
```

Функция**socket\_read()** читає дані з екземпляра [Socket](class.socket.md) `socket`, созданного при помощи функций[socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md)створений за допомогою функцій [socket\_create()](function.socket-create.md) або [socket\_accept()](function.socket-accept.md)

`length`

Максимальна кількість байт для читання визначена параметром `length`. Як варіант ви можете використати **`\r`** **`\n`**, или\*\*`\0`\*\*для окончания чтения (в зависимости от параметра`mode`, Дивіться нижче).

`mode`

Необов'язковий параметр `mode` - це іменована константа:

-   **`PHP_BINARY_READ`**(За замовчуванням) – використовується системна функція`recv()`. Безпечно читати бінарних даних.
-   \*\*`PHP_NORMAL_READ`\*\*- Читання зупиняється на`\n`или`\r`

### Значення, що повертаються

**socket\_read()** повертає дані у вигляді рядка у разі успішного виконання, або **`false`** у разі виникнення помилки (включаючи випадок, коли віддалений хост закрив з'єднання). Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

> **Зауваження** :
> 
> **socket\_read()** повертає рядок нульової довжини (""), коли немає даних для читання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_accept()](function.socket-accept.md) \- приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
-   [socket\_write()](function.socket-write.md) \- Запис у сокет
