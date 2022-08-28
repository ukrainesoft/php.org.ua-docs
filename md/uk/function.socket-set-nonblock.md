Встановлює неблокуючий режим файлового дескриптора fd

-   [« socket\_set\_block](function.socket-set-block.html)
    
-   [socket\_set\_option »](function.socket-set-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Встановлює неблокуючий режим файлового дескриптора fd
    

# socketsetnonblock

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketsetnonblock — Встановлює неблокуючий режим файлового дескриптора fd

### Опис

```methodsynopsis
socket_set_nonblock(Socket $socket): bool
```

Функція **socketsetnonblock()** встановлює прапор **`O_NONBLOCK`** на сокеті, вказаному у параметрі `socket`

Коли операція (наприклад, отримання, відправлення, з'єднання, прийняття з'єднання, ...) виконується на неблокуючому сокеті, скрипт не припинятиме своє виконання до отримання сигналу або можливості виконати операцію. Якщо операція, що виконується, повинна привести до блокування виконання скрипта, то замість цього викликана функція поверне помилку.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socket\_create()](function.socket-create.html) або [socket\_accept()](function.socket-accept.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання **socketsetnonblock()****

```php
<?php
$socket = socket_create_listen(1223);
socket_set_nonblock($socket);

socket_accept($socket);
?>
```

Цей приклад створює сокет, що слухає, на всіх інтерфейсах на порту 1223 і встановлює сокет в режим **`O_NONBLOCK`**. . [socket\_accept()](function.socket-accept.html) буде негайно повертати помилку, якщо тільки в цей момент немає очікуваного з'єднання.

### Дивіться також

-   [socket\_set\_block()](function.socket-set-block.html) - Встановлює блокуючий режим на сокеті
-   [socket\_set\_option()](function.socket-set-option.html) - Встановлює опції для сокету
-   [stream\_set\_blocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці