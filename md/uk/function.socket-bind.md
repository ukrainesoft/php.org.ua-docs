---
navigation:
  - function.socket-atmark.md: « socket\_atmark
  - function.socket-clear-error.md: socket\_clear\_error »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_bind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_bind

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_bind — Прив'язує ім'я до сокету

### Опис

```methodsynopsis
socket_bind(Socket $socket, string $address, int $port = 0): bool
```

Прив'язує ім'я, вказане у параметрі `address`, к сокету, описанному в параметре`socket`. Це має бути зроблено, перш ніж з'єднання встановлено за допомогою функції [socket\_connect()](function.socket-connect.md) або [socket\_listen()](function.socket-listen.md)

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md)

`address`

Якщо сокет із сімейства **`AF_INET`**, то параметр`address` має бути IP-адресою в записі, розділеному точками (наприклад, `127.0.0.1`

Якщо сокет із сімейства **`AF_UNIX`**, то параметр`address` - це шлях до доменного сокету Unix (наприклад, /tmp/my.sock).

`port`(Optional)

Параметр`port` використовується лише коли ім'я прив'язується до сокету **`AF_INET`**, та вказує порт, на якому будуть слухатися з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Код помилки можна отримати за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Использование функции**socket\_bind()**для установки адреса источника**

```php
<?php
// Создаём новый сокет
$sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

// Приклад списка IP-адресов, которые есть на компьютере
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

> **Зауваження** :
> 
> Ця функція має бути застосована на сокеті перед викликом [socket\_connect()](function.socket-connect.md)

> **Зауваження** :
> 
> Примечание по совместимости с Windows 9x/ME: Функция[socket\_last\_error()](function.socket-last-error.md) може повертати неправильний код помилки при спробі зв'язати з сокетом неправильну адресу, яка не належить вашій машині.

### Дивіться також

-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
-   [socket\_last\_error()](function.socket-last-error.md) \- Повертає останню помилку на сокеті
-   [socket\_strerror()](function.socket-strerror.md) \- Повертає рядок, що описує помилку сокету
