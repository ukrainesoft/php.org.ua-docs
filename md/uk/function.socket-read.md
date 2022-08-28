Читає рядок максимальну довжину байт із сокету

-   [« socket\_listen](function.socket-listen.html)
    
-   [socket\_recv »](function.socket-recv.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Читає рядок максимальну довжину байт із сокету
    

# socketread

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketread — Читає рядок максимальну довжину байт із сокету

### Опис

```methodsynopsis
socket_read(Socket $socket, int $length, int $mode = PHP_BINARY_READ): string|false
```

Функція **socketread()** читає дані з екземпляра [Socket](class.socket.html) `socket`, створеного за допомогою функцій [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html)створений за допомогою функцій [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

`length`

Максимальна кількість байт для читання визначена параметром `length`. Як варіант ви можете використати **`\r`** **`\n`**, або **`\0`** для закінчення читання (залежно від параметра `mode`, Дивіться нижче).

`mode`

Необов'язковий параметр `mode` - це іменована константа:

-   **`PHP_BINARY_READ`** (За замовчуванням) – використовується системна функція `recv()`. Безпечно читати бінарних даних.
-   **`PHP_NORMAL_READ`** - Читання зупиняється на `\n` або `\r`

### Значення, що повертаються

**socketread()** повертає дані у вигляді рядка у разі успішного виконання, або **`false`** у разі виникнення помилки (включаючи випадок, коли віддалений хост закрив з'єднання). Код помилки може бути отриманий за допомогою функції [socket\_last\_error()](function.socket-last-error.html). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

> **Зауваження**
> 
> **socketread()** повертає рядок нульової довжини (""), коли немає даних для читання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_accept()](function.socket-accept.html) - приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.html) - Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету
-   [socket\_write()](function.socket-write.html) - Запис у сокет