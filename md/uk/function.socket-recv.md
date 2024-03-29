---
navigation:
  - function.socket-read.md: « socket\_read
  - function.socket-recvfrom.md: socket\_recvfrom »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_recv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_recv

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_recv — Отримує дані з приєднаного сокету

### Опис

```methodsynopsis
socket_recv(    Socket $socket,    ?string &$data,    int $length,    int $flags): int|false
```

Функция**socket\_recv()** отримує `length` байт даних у буфер `data`из сокета`socket`функция**socket\_recv()** може бути використана для отримання даних із приєднаних сокетів. Додатково, один або більше прапорів можуть бути вказані для зміни поведінки функції.

Параметр`data` передається за посиланням, так що він має бути вказаний у вигляді змінної у списку аргументів. Дані, прочитані із сокету `socket` функцією **socket\_recv()**, будуть повернуті у параметрі `data`

### Список параметрів

`socket`

Параметр`socket` має бути екземпляром [Socket](class.socket.md), попередньо створеним за допомогою функції socket\_create().

`data`

Отримані дані будуть передані до змінної, вказаної у параметрі `data`. Якщо відбувається помилка, якщо з'єднання скинуто, або дані недоступні, параметр `data`будет установлен в\*\*`null`\*\*

`length`

До`length` байт буде отримано з віддаленого хоста.

`flags`

Значение параметра`flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (

**Possible values for`flags`**

| Флаг | Опис |
| --- | --- |
| **`MSG_OOB`** | Обробляти позасмугові (out-of-band) дані. |
| **`MSG_PEEK`** | Отримувати дані з початку черги отримання без видалення їх із черги. |
| **`MSG_WAITALL`** | Функція блокуватиме виконання скрипту доти, доки як мінімум `length` байт не буде отримано. Проте, якщо отриманий сигнал або віддалений хост від'єднався, функція може повернути менше даних. |
| **`MSG_DONTWAIT`** | Якщо цей прапор встановлений, то функція повернеться навіть у тому випадку, якщо вона зазвичай блокувала виконання скрипта. |

### Значення, що повертаються

**socket\_recv()** повертає кількість отриманих байтів або **`false`** у разі виникнення помилки. Фактичний код помилки може бути отриманий за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Цей код помилки може бути переданий функції [socket\_strerror()](function.socket-strerror.md) для отримання текстового опису помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання** socket\_recv()\*\*\*\*

Цей приклад - просто варіант першого прикладу статті [Приклади](sockets.examples.md) с использованием**socket\_recv()**

```php
<?php
error_reporting(E_ALL);

echo "<h2>Соединение TCP/IP</h2>\n";

/* Получить порт сервиса WWW. */
$service_port = getservbyname('www', 'tcp');

/* Получить IP-адрес целевого хоста. */
$address = gethostbyname('www.example.com');

/* Создать сокет TCP/IP. */
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === false) {
    echo "Не удалось выполнить функцию socket_create(): причина: " . socket_strerror(socket_last_error()) . "\n";
} else {
    echo "OK.\n";
}

echo "Попытка соединиться с хостом '$address' по порту '$service_port'...";
$result = socket_connect($socket, $address, $service_port);
if ($result === false) {
    echo "Не получилось выполнить функцию socket_connect().\nПричина: ($result) " . socket_strerror(socket_last_error($socket)) . "\n";
} else {
    echo "OK.\n";
}

$in = "HEAD / HTTP/1.1\r\n";
$in .= "Host: www.example.com\r\n";
$in .= "Connection: Close\r\n\r\n";
$out = '';

echo "Отправка запроса HTTP HEAD...";
socket_write($socket, $in, strlen($in));
echo "OK.\n";

echo "Получение ответа:\n\n";
$buf = 'Это мой буфер.';
if (false !== ($bytes = socket_recv($socket, $buf, 2048, MSG_WAITALL))) {
    echo "Прочитано $bytes байта из функции socket_recv(). Закрываем сокет...";
} else {
    echo "Не получилось выполнить socket_recv(); причина: " . socket_strerror(socket_last_error($socket)) . "\n";
}
socket_close($socket);

echo $buf . "\n";
echo "OK.\n\n";
?>
```

Приклад вище виведе щось на зразок такого:

```
<h2>Соединение TCP/IP</h2>
OK.
Попытка соединиться с хостом '208.77.188.166' on port '80'...OK.
Отправка запроса HTTP HEAD...OK.
Получение ответа:

Прочитано 123 байта из функции socket_recv(). Закрываем сокет...HTTP/1.1 200 OK
Date: Mon, 14 Sep 2009 08:56:36 GMT
Server: Apache/2.2.3 (Red Hat)
Last-Modified: Tue, 15 Nov 2005 13:24:10 GMT
ETag: "b80f4-1b6-80bfd280"
Accept-Ranges: bytes
Content-Length: 438
Connection: close
Content-Type: text/html; charset=UTF-8

OK.
```
