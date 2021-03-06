- [«Зумовлені константи](sockets.constants.md)
- [Помилки сокетів »](sockets.errors.md)

- [PHP Manual](index.md)
- [Сокети](book.sockets.md)
- Приклади

# Приклади

**Приклад #1 Приклад використання сокетів: Простий сервер TCP/IP**

Цей приклад показує роботу простого сервера. Змініть змінні
`address` та `port` відповідно до ваших налаштувань і виконайте.
Потім ви можете з'єднатися з сервером із командою, схожою на: **telnet
192.168.1.53 10000** (де адреса та порт повинні відповідати вашим
налаштувань). Все, що ви наберете на клавіатурі, буде виведено на
сервері та відправлено вам назад. Щоб вимкнути, наберіть 'вихід'.

` #!/usr/local/bin/php -q<?phperror_reporting(E_ALL);/* Дозволяє скрипту чекати з'єднання нескінченно. */set_time_limit(0);/* Включає приховане очищення висновку так, ми ми бачимо дані ** як тільки вони з'являються. */ob_implicit_flush();$address = '192.168.1.53';$port = 10000;if (($sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP)) =   причина: " . socket_strerror(socket_last_error()) . "
";}if(socket_bind($sock, $address, $port) === false) {   echo "Не удалося виконати socket_bind(): причина: "' . socket_strerror(so$las)
";}if(socket_listen($sock, 5) === false) {    echo "Не удалося виконати socket_listen(): причина: " . socket_strerror(socket_last_error($so)
";}do {    if (($msgsock = socket_accept($sock)) === false) {        echo "Не удалося виконано socket_accept(): |
";        break;    }    /* Відправляємо інструкції. */   $msg = "
Ласкаво просимо на тестовий сервер PHP.
Щоб відключитися, наберіть вихід. Щоб вимкнути сервер, наберіть вимикання.
";    socket_write($msgsock, $msg, strlen($msg));    do {        if (false === ($buf = socket_read($msgsock, 2048, PHP_NORMAL_READ))) {            echo "Не удалось выполнить socket_read(): причина: " . socket_strerror(socket_last_error($msgsock)) . "
";            break 2;        }        if (!$buf = trim($buf)) {            continue;        }        if ($buf == 'выход') {            break;        }        if ($buf == 'выключение') {            socket_close($ msgsock);             break 2;       }        $talkback = "PHP: Ви сказали '$bu'.
";    socket_write($msgsock, $talkback, strlen($talkback));        echo "$buf
";    } while (true);    socket_close($msgsock);} while (true);socket_close($sock);?> `

**Приклад #2 Приклад використання сокетів: Простий клієнт TCP/IP**

Цей приклад показує використання простого одноразового HTTP-клієнта.
Він просто з'єднується зі сторінкою, надсилає запит HEAD, виводить
відповідь та завершує роботу.

` <?phperror_reporting(E_ALL);echo "<h2>З'єднанняTCP/IP</h2>
";/* Отримуємо порт сервісу WWW. */$service_port = getservbyname('www', 'tcp');/* Отримуємо IP-адресу цільового хоста. */$address = gethostbyname('www; /* Створюємо сокет TCP/IP. */$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);if ($socket === false) {? ) . "
";} else {    echo "OK.
";}echo "Намагаємося з'єднатися з '$address' на порту '$service_port'...";$result = socket_connect($socket, $address, $service_port);if ($result === false)      Не вдалося виконати socket_connect ().
Причина: ($result) " . socket_strerror(socket_last_error($socket)) . "
";} else {    echo "OK.
";}$in = "HEAD / HTTP/1.1
";$in .= "Host: www.example.com
";$in .= "Connection: Close

";$out = '';echo "Відправляємо HTTP-запит HEAD...";socket_write($socket, $in, strlen($in));echo "OK.
";echo "Читаємо відповідь:

";while ($out = socket_read($socket, 2048)) {    echo $out;}echo "Закриваємо сокет...";socket_close($socket);echo "OK.

";?> `
