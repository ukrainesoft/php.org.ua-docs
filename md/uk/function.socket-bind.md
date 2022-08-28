Прив'язує ім'я до сокету

-   [« socket\_addrinfo\_lookup](function.socket-addrinfo-lookup.html)
    
-   [socket\_clear\_error »](function.socket-clear-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Прив'язує ім'я до сокету
    

# socketbind

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketbind — Прив'язує ім'я до сокету

### Опис

```methodsynopsis
socket_bind(Socket $socket, string $address, int $port = 0): bool
```

Прив'язує ім'я, вказане у параметрі `address`до сокету, описаного у параметрі `socket`. Це має бути зроблено, перш ніж з'єднання встановлено за допомогою функції [socket\_connect()](function.socket-connect.html) або [socket\_listen()](function.socket-listen.html)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socket\_create()](function.socket-create.html)

`address`

Якщо сокет із сімейства **`AF_INET`**, то параметр `address` має бути IP-адресою в записі, розділеному точками (наприклад, `127.0.0.1`

Якщо сокет із сімейства **`AF_UNIX`**, то параметр `address` - це шлях до доменного сокету Unix (наприклад, /tmp/my.sock).

`port` (Optional)

Параметр `port` використовується лише коли ім'я прив'язується до сокету **`AF_INET`**, та вказує порт, на якому будуть слухатися з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Код помилки може бути отриманий за допомогою функції [socket\_last\_error()](function.socket-last-error.html). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.html) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Використання функції **socketbind()** для встановлення адреси джерела**

```php
<?php
// Создаём новый сокет
$sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

// Пример списка IP-адресов, которые есть на компьютере
$sourceips['kevin']    = '127.0.0.1';
$sourceips['madcoder'] = '127.0.0.2';

// Привязываем адрес источника
socket_bind($sock, $sourceips['madcoder']);

// Соединяемся с адресом назначения
socket_connect($sock, '127.0.0.1', 80);

// Пишем в сокет
$request = 'GET / HTTP/1.1' . "\r\n" .
           'Host: example.com' . "\r\n\r\n";
socket_write($sock, $request);

// Закрываем сокет
socket_close($sock);

?>
```

### Примітки

> **Зауваження**
> 
> Ця функція має бути застосована на сокеті перед викликом [socket\_connect()](function.socket-connect.html)

> **Зауваження**
> 
> Примітка щодо сумісності з Windows 9x/ME: Функція [socket\_last\_error()](function.socket-last-error.html) може повертати неправильний код помилки при спробі зв'язати з сокетом неправильну адресу, яка не належить вашій машині.

### Дивіться також

-   [socket\_connect()](function.socket-connect.html) - Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_last\_error()](function.socket-last-error.html) - Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.html) - Повертає рядок, що описує помилку сокету