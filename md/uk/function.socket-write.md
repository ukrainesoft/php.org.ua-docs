---
navigation:
  - function.socket-strerror.md: « socket\_strerror
  - function.socket-wsaprotocol-info-export.md: socket\_wsaprotocol\_info\_export »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_write

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_write — Запис у сокет

### Опис

```methodsynopsis
socket_write(Socket $socket, string $data, ?int $length = null): int|false
```

Функция**socket\_write()** записує в сокет `socket` дані із зазначеного буфера `data`

### Список параметрів

`socket`

`data`

Буфер, який буде записано.

`length`

Необов'язковий параметр `length` може вказувати інше число байт, що записуються в сокет. Якщо це число більше, ніж довжина буфера, воно буде мовчки урізано до довжини буфера.

### Значення, що повертаються

Повертає кількість байт, успішно записаних у сокет або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

> **Зауваження** :
> 
> Цілком нормально для функції **socket\_write()** повертати нуль, що означає, що жодного байта не було записано. Будь ласка, використовуйте оператор `===`для проверки значения на\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
| 8.0.0 | `length` тепер допускає значення null. |

### Примітки

> **Зауваження** :
> 
> **socket\_write()** не обов'язково записує всі байти із зазначеного буфера. Нормально те, що, залежно від мережевих буферів і т. д., лише кілька даних, навіть один байт, буде записаний, хоча ваш буфер більше. Ви повинні стежити за тим, щоб ненавмисно не забути передати залишок ваших даних.

### Дивіться також

-   [socket\_accept()](function.socket-accept.md) \- приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_read()](function.socket-read.md) \- Читає рядок максимальну довжину байт із сокету
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
