---
navigation:
  - function.socket-addrinfo-lookup.md: « socketaddrinfolookup
  - function.socket-clear-error.md: socketclearerror »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketbind
---
# socketbind

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketbind — Прив'язує ім'я до сокету

### Опис

```methodsynopsis
socket_bind(Socket $socket, string $address, int $port = 0): bool
```

Прив'язує ім'я, вказане у параметрі `address`до сокету, описаного у параметрі `socket`. Це має бути зроблено, перш ніж з'єднання встановлено за допомогою функції [socketconnect()](function.socket-connect.md) або [socketlisten()](function.socket-listen.md)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socketcreate()](function.socket-create.md)

`address`

Якщо сокет із сімейства **`AF_INET`**, то параметр `address` має бути IP-адресою в записі, розділеному точками (наприклад, `127.0.0.1`

Якщо сокет із сімейства **`AF_UNIX`**, то параметр `address` - це шлях до доменного сокету Unix (наприклад, /tmp/my.sock).

`port` (Optional)

Параметр `port` використовується лише коли ім'я прив'язується до сокету **`AF_INET`**, та вказує порт, на якому будуть слухатися з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Код помилки може бути отриманий за допомогою функції [socketlasterror()](function.socket-last-error.md). Цей код може бути переданий функції [socketstrerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Використання функції **socketbind()** для встановлення адреси джерела**

```php
<?php
// Создаём новый сокет
$sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

// Пример списка IP-адресов, которые есть на компьютере
$sourceips['kevin']    = '127.0.0.1';
$sourceips['madcoder'] = '127.0.0.2';

// Привязываем адрес источника
socket_bind($sock, $sourceips['madcoder']);

// Соединяемся с адресом назначения
socket_connect($sock, '127.0.0.1', 80);

// Пишем в сокет
$request = 'GET / HTTP/1.1' . "\r\n" .
           'Host: example.com' . "\r\n\r\n";
socket_write($sock, $request);

// Закрываем сокет
socket_close($sock);

?>
```

### Примітки

> **Зауваження**
> 
> Ця функція має бути застосована на сокеті перед викликом [socketconnect()](function.socket-connect.md)

> **Зауваження**
> 
> Примітка щодо сумісності з Windows 9x/ME: Функція [socketlasterror()](function.socket-last-error.md) може повертати неправильний код помилки при спробі зв'язати з сокетом неправильну адресу, яка не належить вашій машині.

### Дивіться також

-   [socketconnect()](function.socket-connect.md) - Починає з'єднання із сокетом
-   [socketlisten()](function.socket-listen.md) - Прослуховує вхідні з'єднання на сокеті
-   [socketcreate()](function.socket-create.md) - створює сокет (кінцеву точку для обміну інформацією)
-   [socketlasterror()](function.socket-last-error.md) - Повертає останню помилку на сокеті
-   [socketstrerror()](function.socket-strerror.md) - Повертає рядок, що описує помилку сокету
