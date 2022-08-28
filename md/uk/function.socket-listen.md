Прослуховує вхідні з'єднання на сокеті

-   [« socket\_last\_error](function.socket-last-error.html)
    
-   [socket\_read »](function.socket-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Прослуховує вхідні з'єднання на сокеті
    

# socketlisten

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketlisten — Прослуховує вхідні з'єднання на сокеті

### Опис

```methodsynopsis
socket_listen(Socket $socket, int $backlog = 0): bool
```

Після того, як сокет `socket` був створений за допомогою функції [socket\_create()](function.socket-create.html) та прив'язаний до імені за допомогою функції [socket\_bind()](function.socket-bind.html), йому можна вказати слухати вхідні з'єднання на сокеті `socket`

Функція **socketlisten()** застосовна тільки до сокетів типу **`SOCK_STREAM`** або **`SOCK_SEQPACKET`**

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html)створений за допомогою функцій [socket\_create()](function.socket-create.html) або [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html)

`backlog`

Максимум `backlog` вхідних з'єднань буде поміщено у чергу на обробку. Якщо запит на з'єднання прийде, коли черга заповнена, клієнт може отримати помилку `ECONNREFUSED`, або, якщо базовий протокол дозволяє повторну передачу, запит буде повторено.

> **Зауваження**
> 
> Максимальне значення параметра `backlog` дуже залежить використовується платформи. У Linux дуже велике значення буде мовчки обрізано до **`SOMAXCONN`**. У win32, якщо передано **`SOMAXCONN`**, базовий провайдер сервісу, відповідального за сокет, встановить цей параметр максимальним *розумним* значенням. Немає стандартного способу дізнатися про актуальне значення "backlog" для цієї платформи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки може бути отриманий за допомогою функції [socket\_last\_error()](function.socket-last-error.html). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_accept()](function.socket-accept.html) - приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.html) - Починає з'єднання із сокетом
-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету
-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html) - Створити та прив'язати до сокету із зазначеного addrinfo