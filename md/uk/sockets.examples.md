---
navigation:
  - sockets.constants.html: « Обумовлені константи
  - sockets.errors.html: Ошибки сокетів »
  - index.html: PHP Manual
  - book.sockets.html: Сокети
title: Приклади
---
# Приклади

**Приклад #1 Приклад використання сокетів: Простий сервер TCP/IP**

Цей приклад показує роботу простого сервера. Змініть змінні address та port відповідно до ваших налаштувань і виконайте. Потім ви можете з'єднатися з сервером із командою, схожою на: **telnet 192.168.1.53 10000** (де адреса та порт повинні відповідати вашим налаштуванням). Все, що ви наберете на клавіатурі, буде виведено на сервері і відправлено вам назад. Щоб вимкнути, наберіть 'вихід'.

```php
#!/usr/local/bin/php -q
<?php
error_reporting(E_ALL);

/* Позволяет скрипту ожидать соединения бесконечно. */
set_time_limit(0);

/* Включает скрытое очищение вывода так, что мы видим данные
 * как только они появляются. */
ob_implicit_flush();

$address = '192.168.1.53';
$port = 10000;

if (($sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP)) === false) {
    echo "Не удалось выполнить socket_create(): причина: " . socket_strerror(socket_last_error()) . "\n";
}

if (socket_bind($sock, $address, $port) === false) {
    echo "Не удалось выполнить socket_bind(): причина: " . socket_strerror(socket_last_error($sock)) . "\n";
}

if (socket_listen($sock, 5) === false) {
    echo "Не удалось выполнить socket_listen(): причина: " . socket_strerror(socket_last_error($sock)) . "\n";
}

do {
    if (($msgsock = socket_accept($sock)) === false) {
        echo "Не удалось выполнить socket_accept(): причина: " . socket_strerror(socket_last_error($sock)) . "\n";
        break;
    }
    /* Отправляем инструкции. */
    $msg = "\nДобро пожаловать на тестовый сервер PHP. \n" .
        "Чтобы отключиться, наберите 'выход'. Чтобы выключить сервер, наберите 'выключение'.\n";
    socket_write($msgsock, $msg, strlen($msg));

    do {
        if (false === ($buf = socket_read($msgsock, 2048, PHP_NORMAL_READ))) {
            echo "Не удалось выполнить socket_read(): причина: " . socket_strerror(socket_last_error($msgsock)) . "\n";
            break 2;
        }
        if (!$buf = trim($buf)) {
            continue;
        }
        if ($buf == 'выход') {
            break;
        }
        if ($buf == 'выключение') {
            socket_close($msgsock);
            break 2;
        }
        $talkback = "PHP: Вы сказали '$buf'.\n";
        socket_write($msgsock, $talkback, strlen($talkback));
        echo "$buf\n";
    } while (true);
    socket_close($msgsock);
} while (true);

socket_close($sock);
?>
```

**Приклад #2 Приклад використання сокетів: Простий клієнт TCP/IP**

Цей приклад показує використання простого одноразового HTTP-клієнта. Він просто з'єднується зі сторінкою, надсилає запит HEAD, виводить відповідь та завершує роботу.

```php
<?php
error_reporting(E_ALL);

echo "<h2>Соединение TCP/IP</h2>\n";

/* Получаем порт сервиса WWW. */
$service_port = getservbyname('www', 'tcp');

/* Получаем IP-адрес целевого хоста. */
$address = gethostbyname('www.example.com');

/* Создаём сокет TCP/IP. */
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === false) {
    echo "Не удалось выполнить socket_create(): причина: " . socket_strerror(socket_last_error()) . "\n";
} else {
    echo "OK.\n";
}

echo "Пытаемся соединиться с '$address' на порту '$service_port'...";
$result = socket_connect($socket, $address, $service_port);
if ($result === false) {
    echo "Не удалось выполнить socket_connect().\nПричина: ($result) " . socket_strerror(socket_last_error($socket)) . "\n";
} else {
    echo "OK.\n";
}

$in = "HEAD / HTTP/1.1\r\n";
$in .= "Host: www.example.com\r\n";
$in .= "Connection: Close\r\n\r\n";
$out = '';

echo "Отправляем HTTP-запрос HEAD...";
socket_write($socket, $in, strlen($in));
echo "OK.\n";

echo "Читаем ответ:\n\n";
while ($out = socket_read($socket, 2048)) {
    echo $out;
}

echo "Закрываем сокет...";
socket_close($socket);
echo "OK.\n\n";
?>
```
