Відкриває сокет на вказаному порту для прийняття з'єднань

-   [« socket\_connect](function.socket-connect.html)
    
-   [socket\_create\_pair »](function.socket-create-pair.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Відкриває сокет на вказаному порту для прийняття з'єднань
    

# socketcreatelisten

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketcreatelisten — Відкриває сокет на вказаному порту для отримання з'єднань

### Опис

```methodsynopsis
socket_create_listen(int $port, int $backlog = 128): Socket|false
```

**socketcreatelisten()** створює новий екземпляр [Socket](class.socket.html) типу **`AF_INET`**слухає на *всіх* локальних інтерфейсів вказаний порт в очікуванні нових з'єднань.

Ця функція призначена для спрощення завдання створення нового сокету, який слухає порт для отримання нових з'єднань.

### Список параметрів

`port`

Порт, який слід слухати на всіх інтерфейсах.

`backlog`

Параметр `backlog` визначає максимальну довжину, до якої може зрости черга з'єднань, що очікують. . **`SOMAXCONN`** може бути переданий як параметр `backlog`, дивіться [socket\_listen()](function.socket-listen.html) для повнішої інформації.

### Значення, що повертаються

**socketcreatelisten()** повертає новий екземпляр [Socket](class.socket.html) у разі успішного виконання або **`false`** у разі виникнення помилки. Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.html). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.html); раніше повертався ресурс (resource). |

### Примітки

> **Зауваження**
> 
> Якщо ви хочете створити сокет, який прослуховуватиме лише певний інтерфейс, вам потрібно використовувати функції [socket\_create()](function.socket-create.html) [socket\_bind()](function.socket-bind.html) і [socket\_listen()](function.socket-listen.html)

### Дивіться також

-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_create\_pair()](function.socket-create-pair.html) - Створює пару нерозрізнених сокетів та зберігає їх у масиві
-   [socket\_bind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету