Отримує дані з приєднаного сокету

-   [« socketread](function.socket-read.html)
    
-   [socketrecvfrom »](function.socket-recvfrom.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Отримує дані з приєднаного сокету
    

# socketrecv

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketrecv — Отримує дані з приєднаного сокету

### Опис

```methodsynopsis
socket_recv(    Socket $socket,    ?string &$data,    int $length,    int $flags): int|false
```

Функція **socketrecv()** отримує `length` байт даних у буфер `data` із сокету `socket`. функція **socketrecv()** може бути використана для отримання даних із приєднаних сокетів. Додатково, один або більше прапорів можуть бути вказані для зміни поведінки функції.

Параметр `data` передається за посиланням, так що він має бути вказаний у вигляді змінної у списку аргументів. Дані, прочитані із сокету `socket` функцією **socketrecv()**, будуть повернуті у параметрі `data`

### Список параметрів

`socket`

Параметр `socket` має бути екземпляром [Socket](class.socket.html), попередньо створеним за допомогою функції socketcreate().

`data`

Отримані дані будуть передані до змінної, вказаної у параметрі `data`. Якщо відбувається помилка, якщо з'єднання скинуто, або дані недоступні, параметр `data` буде встановлений у **`null`**

`length`

До `length` байт буде отримано з віддаленого хоста.

`flags`

Значення параметру `flags` може бути будь-якою комбінацією наступних прапорів, з'єднаних за допомогою бінарного оператора OR (`|`

**Можливі values ​​for `flags`**

| Флаг | Описание |
| --- | --- |
| **`MSG_OOB`** | Обробляти позасмугові (out-of-band) дані. |
| **`MSG_PEEK`** | Отримувати дані від початку черги отримання без видалення їх із черги. |
| **`MSG_WAITALL`** | Функція блокуватиме виконання скрипту доти, доки як мінімум `length` байт не буде отримано. Проте, якщо отриманий сигнал або віддалений хост від'єднався, функція може повернути менше даних. |
| **`MSG_DONTWAIT`** | Якщо цей прапор встановлений, то функція повернеться навіть у тому випадку, якщо вона зазвичай блокувала виконання скрипта. |

### Значення, що повертаються

**socketrecv()** повертає кількість отриманих байтів або **`false`** у разі виникнення помилки. Фактичний код помилки може бути отриманий за допомогою функції [socketlasterror()](function.socket-last-error.html). Цей код помилки може бути переданий функції [socketstrerror()](function.socket-strerror.html) для отримання текстового опису помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |

### Приклади

**Приклад #1 Приклад використання **socketrecv()****

Цей приклад - просто варіант першого прикладу статті [Приклади](sockets.examples.html) з використанням **socketrecv()**

```php
<?php
error_reporting(E_ALL);

echo "<h2>Соединение TCP/IP</h2>\n";

/* Получить порт сервиса WWW. */
$service_port = getservbyname('www', 'tcp');

/* Получить IP-адрес целевого хоста. */
$address = gethostbyname('www.example.com');

/* Создать сокет TCP/IP. */
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === false) {
    echo "Не удалось выполнить функцию socket_create(): причина: " . socket_strerror(socket_last_error()) . "\n";
} else {
    echo "OK.\n";
}

echo "Попытка соединиться с хостом '$address' по порту '$service_port'...";
$result = socket_connect($socket, $address, $service_port);
if ($result === false) {
    echo "Не получилось выполнить функцию socket_connect().\nПричина: ($result) " . socket_strerror(socket_last_error($socket)) . "\n";
} else {
    echo "OK.\n";
}

$in = "HEAD / HTTP/1.1\r\n";
$in .= "Host: www.example.com\r\n";
$in .= "Connection: Close\r\n\r\n";
$out = '';

echo "Отправка запроса HTTP HEAD...";
socket_write($socket, $in, strlen($in));
echo "OK.\n";

echo "Получение ответа:\n\n";
$buf = 'Это мой буфер.';
if (false !== ($bytes = socket_recv($socket, $buf, 2048, MSG_WAITALL))) {
    echo "Прочитано $bytes байта из функции socket_recv(). Закрываем сокет...";
} else {
    echo "Не получилось выполнить socket_recv(); причина: " . socket_strerror(socket_last_error($socket)) . "\n";
}
socket_close($socket);

echo $buf . "\n";
echo "OK.\n\n";
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