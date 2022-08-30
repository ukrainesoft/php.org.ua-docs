Повертає останню помилку на сокеті

-   [« socketimportstream](function.socket-import-stream.html)
    
-   [socketlisten »](function.socket-listen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Повертає останню помилку на сокеті
    

# socketlasterror

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketlasterror — Повертає останню помилку на сокеті

### Опис

```methodsynopsis
socket_last_error(?Socket $socket = null): int
```

Якщо екземпляр [Socket](class.socket.html) передано цю функцію, то повертається остання помилка, яка сталася на цьому конкретному сокеті. Якщо `socket` не вказано, повертається код помилки останньої функції сокетів. Останнє особливо корисне для таких функцій, як [socketcreate()](function.socket-create.html), яка не повертає сокет у разі невдачі та [socketselect()](function.socket-select.html), що може закінчитися невдало з причин, не пов'язаних безпосередньо з конкретним сокетом. Код помилки підходить для передачі функції [socketstrerror()](function.socket-strerror.html), яка повертає рядок, що описує вказаний код помилки.

Якщо помилок немає або вони були очищені функцією [socketclearerror()](function.socket-clear-error.html), функція поверне `0`

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socketcreate()](function.socket-create.html)

### Значення, що повертаються

Ця функція повертає код помилки сокету.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |
|  | `socket` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **socketlasterror()****

```php
<?php
$socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if ($socket === false) {
    $errorcode = socket_last_error();
    $errormsg = socket_strerror($errorcode);

    die("Не могу создать сокет: [$errorcode] $errormsg");
}
?>
```

### Примітки

> **Зауваження**
> 
> **socketlasterror()** не очищає код помилки, використовуйте [socketclearerror()](function.socket-clear-error.html) для цієї мети.