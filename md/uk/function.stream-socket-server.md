Створює інтернет-сокет або доменний сокет Unix

-   [« stream\_socket\_sendto](function.stream-socket-sendto.html)
    
-   [stream\_socket\_shutdown »](function.stream-socket-shutdown.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Створює інтернет-сокет або доменний сокет Unix
    

# streamsocketserver

(PHP 5, PHP 7, PHP 8)

streamsocketserver — Створює інтернет-сокет або доменний сокет Unix

### Опис

```methodsynopsis
stream_socket_server(    string $address,    int &$error_code = null,    string &$error_message = null,    int $flags = STREAM_SERVER_BIND | STREAM_SERVER_LISTEN,    ?resource $context = null): resource|false
```

Створює сокет потоку чи датаграми на вказаному `address`

Ця функція створює тільки сокет. Щоб почати приймати з'єднання, використовуйте [stream\_socket\_accept()](function.stream-socket-accept.html)

### Список параметрів

`address`

Тип сокету, що створюється, визначається по транспорту, вказаному з використанням стандартного форматування URL: `transport://target`

Для доменних сокетів інтернету (**`AF_INET`**), таких як TCP та UDP, частина `target` параметра `remote_socket` повинна складатися з імені хоста або IP-адреси з наступною двокрапкою та номером порту. Для доменних сокетів Unix частина `target` має вказувати на файл сокета у файловій системі.

Залежно від оточення, доменні сокети Unix можуть бути недоступними. Список доступних транспортів можна отримати за допомогою функції [stream\_get\_transports()](function.stream-get-transports.html). Дивіться [Список поддерживаемых транспортных протоколов](transports.html) для переліку вбудованих транспортів.

`error_code`

Якщо необов'язкові аргументи `error_code` і `error_message` присутні, вони будуть встановлені для вказівки дійсного рівня системної помилки, яка відбувається при системних викликах `socket()` `bind()` і `listen()`. Якщо значення, що повертається в `error_code`, одно `0` та функція повернула **`false`**Це означає, що помилка сталася до виклику `bind()`. Швидше за все це сталося через проблему ініціалізації сокету. Візьміть до уваги, що аргументи `error_code` і `error_message` повинні завжди передаватися за посиланням.

`error_message`

Дивіться опис параметра `error_code`

`flags`

Бітова маска, яка може бути встановлена ​​в будь-якій комбінації прапорів для створення сокету.

> **Зауваження**
> 
> Для UDP-сокетів ви повинні використовувати **`STREAM_SERVER_BIND`** як параметр `flags`

`context`

### Значення, що повертаються

Повертає створений потік або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                         |
|--------|--------------------------------------------------|
|        | Параметр `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання серверних сокетів TCP**

```php
<?php
$socket = stream_socket_server("tcp://0.0.0.0:8000", $errno, $errstr);
if (!$socket) {
  echo "$errstr ($errno)<br />\n";
} else {
  while ($conn = stream_socket_accept($socket)) {
    fwrite($conn, 'Локальное время ' . date('n/j/Y g:i a') . "\n");
    fclose($conn);
  }
  fclose($socket);
}
?>
```

Приклад нижче показує, як працювати як сервер часу, який може відповідати на запити часу, як показано в прикладі функції [stream\_socket\_client()](function.stream-socket-client.html)

> **Зауваження**: Більшість систем вимагають доступу з правами root для створення серверного сокету на порту нижче, ніж 1024.

**Приклад #2 Приклад використання серверних сокетів UDP**

```php
<?php
$socket = stream_socket_server("udp://127.0.0.1:1113", $errno, $errstr, STREAM_SERVER_BIND);
if (!$socket) {
    die("$errstr ($errno)");
}

do {
    $pkt = stream_socket_recvfrom($socket, 1, 0, $peer);
    echo "$peer\n";
    stream_socket_sendto($socket, date("D M j H:i:s Y\r\n"), 0, $peer);
} while ($pkt !== false);

?>
```

### Примітки

> **Зауваження**: Якщо вказати числову адресу IPv6 (наприклад, `fe80::1`) Ви повинні укладати його в квадратні дужки. Наприклад, `tcp://[fe80::1]:80`

### Дивіться також

-   [stream\_socket\_client()](function.stream-socket-client.html) - Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_set\_blocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.html) - Встановити значення часу очікування потоку
-   [fgets()](function.fgets.html) - Читає рядок із файлу
-   [fgetss()](function.fgetss.html) - Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.html) - Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.html) - Закриває відкритий дескриптор файлу
-   [feof()](function.feof.html) - Перевіряє, чи кінець файлу досягнуто
-   [Модуль curl](ref.curl.html)