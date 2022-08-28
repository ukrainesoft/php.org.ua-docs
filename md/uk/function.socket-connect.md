Починає з'єднання із сокетом

-   [« socket\_cmsg\_space](function.socket-cmsg-space.html)
    
-   [socket\_create\_listen »](function.socket-create-listen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Починає з'єднання із сокетом
    

# socketconnect

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketconnect — Починає з'єднання з сокетом

### Опис

```methodsynopsis
socket_connect(Socket $socket, string $address, ?int $port = null): bool
```

Ініціалізує з'єднання з адресою `address`, використовуючи екземпляр [Socket](class.socket.html) `socket`, який має бути екземпляром [Socket](class.socket.html), створеним за допомогою функції [socket\_create()](function.socket-create.html)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою [socket\_create()](function.socket-create.html)

`address`

Параметр `address` може бути IPv4-адресою в записі, розділеною точками (наприклад, `127.0.0.1`), якщо параметр `socket` дорівнює **`AF_INET`**, правильна IPv6-адреса (наприклад, `::1`), якщо включена підтримка IPv6 та параметр `socket` дорівнює **`AF_INET6`** або шлях до файлу доменного сокету Unix, якщо використовується сімейство сокетів **`AF_UNIX`**

`port`

Параметр `port` використовується та обов'язковий тільки в тому випадку, якщо відбувається з'єднання з сокетом **`AF_INET`** або **`AF_INET6`**, і він вказує порт на віддаленому хості, до якого має бути створено з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.html). Цей код може бути потім переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

> **Зауваження**
> 
> Якщо неблокуючий сокет, то ця функція повертає **`false`** з помилкою `Operation now in progress`

### список змін

| Версия | Описание                                                                                    |
|--------|---------------------------------------------------------------------------------------------|
|        | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |
|        | `port` тепер допускає значення null.                                                        |

### Дивіться також

-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету