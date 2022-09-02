---
navigation:
  - function.socket-strerror.md: « socketstrerror
  - function.socket-wsaprotocol-info-export.md: socketwsaprotocolinfoexport »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketwrite
---
# socketwrite

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketwrite — Запис у сокет

### Опис

```methodsynopsis
socket_write(Socket $socket, string $data, ?int $length = null): int|false
```

Функція **socketwrite()** записує в сокет `socket` дані із зазначеного буфера `data`

### Список параметрів

`socket`

`data`

Буфер, який буде записано.

`length`

Необов'язковий параметр `length` може вказувати інше число байт, що записуються в сокет. Якщо це число більше, ніж довжина буфера, воно буде мовчки урізано до довжини буфера.

### Значення, що повертаються

Повертає кількість байт, успішно записаних у сокет або **`false`** у разі виникнення помилки. Код помилки може бути отриманий за допомогою функції [socketlasterror()](function.socket-last-error.md). Цей код може бути переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

> **Зауваження**
> 
> Цілком нормально для функції **socketwrite()** повертати нуль, що означає, що жодного байта не було записано. Будь ласка, використовуйте оператор `===` для перевірки значення на **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
|  | `length` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> **socketwrite()** не обов'язково записує всі байти із зазначеного буфера. Нормально те, що, залежно від мережевих буферів і т. д., лише кілька даних, навіть один байт, буде записаний, хоча ваш буфер більше. Ви повинні стежити за тим, щоб ненавмисно не забути передати залишок ваших даних.

### Дивіться також

-   [socketaccept()](function.socket-accept.md) - приймає з'єднання на сокеті
-   [socketbind()](function.socket-bind.md) - Прив'язує ім'я до сокету
-   [socketconnect()](function.socket-connect.md) - Починає з'єднання із сокетом
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketread()](function.socket-read.md) - Читає рядок максимальну довжину байт із сокету
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
