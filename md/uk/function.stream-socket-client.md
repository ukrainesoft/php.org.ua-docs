---
navigation:
  - function.stream-socket-accept.md: « stream\_socket\_accept
  - function.stream-socket-enable-crypto.md: stream\_socket\_enable\_crypto »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_client
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_client

(PHP 5, PHP 7, PHP 8)

stream\_socket\_client — Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix

### Опис

```methodsynopsis
stream_socket_client(    string $address,    int &$error_code = null,    string &$error_message = null,    ?float $timeout = null,    int $flags = STREAM_CLIENT_CONNECT,    ?resource $context = null): resource|false
```

Починає з'єднання потоку або датаграми з віддаленим сокетом, зазначеним параметром `address`. Тип сокету, що створюється, визначається по транспорту, вказаному з використанням стандартного форматування URL: `transport://target`. Для інтернет-сокетів, (AF\_INET) таких, як TCP та UDP, частина `target`параметра`address` повинна складатися з імені хоста або IP-адреси, за яким слідує двокрапка та номер порту. Для доменних сокетів Unix, частина `target` має вказувати на файл сокета у файловій системі.

> **Зауваження** :
> 
> За замовчуванням потік буде відкритий у режимі блокування. Ви можете переключити його в режим неблокування, використовуючи функцію [stream\_set\_blocking()](function.stream-set-blocking.md)

### Список параметрів

`address`

Адреса віддаленого сокету для з'єднання.

`error_code`

Буде надано номер системної помилки, якщо з'єднання не вдалося встановити.

`error_message`

Буде надіслано повідомлення про системну помилку, якщо з'єднання не вдалося встановити.

`timeout`

Число секунд, протягом яких має відбутися час очікування системного виклику `connect()`По умолчанию используется значение[default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)

> **Зауваження**: Цей параметр застосовується, лише якщо спроба асинхронного з'єднання не відбувається.

> **Зауваження** :
> 
> Щоб вказати час очікування для читання/запису даних через сокет, скористайтеся функцією [stream\_set\_timeout()](function.stream-set-timeout.md), так как параметр`timeout` застосовується лише під час створення з'єднання через сокет.

`flags`

Поле бітової маски, яке може набувати значення будь-якої комбінації прапорів з'єднання. В даний час набір з'єднань прапорів обмежений такими значеннями **`STREAM_CLIENT_CONNECT`**(по умолчанию),**`STREAM_CLIENT_ASYNC_CONNECT`**и**`STREAM_CLIENT_PERSISTENT`**

`context`

Діючий ресурс контексту, створений за допомогою функції [stream\_context\_create()](function.stream-context-create.md)

### Значення, що повертаються

У разі успішного виконання повертається ресурс потоку, який може бути використаний з іншими файловими функціями (такими як [fgets()](function.fgets.md) [fgetss()](function.fgetss.md) [fwrite()](function.fwrite.md) [fclose()](function.fclose.md), и[feof()](function.feof.md)), у разі виникнення помилки повертається **`false`**

### Помилки

У разі невдалого виклику функції аргументи `error_code`и`error_message` будуть заповнені системною помилкою, яка сталася під час системного виклику `connect()`. Якщо значення, повернене в аргументі `error_code` одно и функция возвратила значение\*\*`false`\*\*Це означає, що помилка сталася до виклику `connect()`. Це сталося, швидше за все, через проблему ініціалізації сокету. Візьміть до уваги, що аргументи `error_code`и`error_message` завжди передаватимуться за посиланням.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timeout`и`context` тепер допускають значення null. |

### Приклади

**Пример #1 Пример использования**stream\_socket\_client()\*\*\*\*

```php
<?php
$fp = stream_socket_client("tcp://www.example.com:80", $errno, $errstr, 30);
if (!$fp) {
    echo "$errstr ($errno)<br />\n";
} else {
    fwrite($fp, "GET / HTTP/1.0\r\nHost: www.example.com\r\nAccept: */*\r\n\r\n");
    while (!feof($fp)) {
        echo fgets($fp, 1024);
    }
    fclose($fp);
}
?>
```

**Приклад #2 Використання UDP-з'єднання**

Отримання дня та часу від UDP-сервісу "daytime" (порт 13) на localhost.

```php
<?php
$fp = stream_socket_client("udp://127.0.0.1:13", $errno, $errstr);
if (!$fp) {
    echo "ОШИБКА: $errno - $errstr<br />\n";
} else {
    fwrite($fp, "\n");
    echo fread($fp, 26);
    fclose($fp);
}
?>
```

### Примітки

**Увага**

UDP-сокети іноді можуть відкриватися без помилки, навіть якщо віддалений хост недоступний. Помилка стане помітною тільки коли ви читатимете або писатимете дані з/в сокет. Причина цього в тому, що UDP - це протокол без з'єднання, що означає, що операційна система не намагається встановити з'єднання з сокетом, поки їй насправді не потрібно відправити або отримати дані.

> **Зауваження**: Якщо вказати числову адресу IPv6 (наприклад, `fe80::1`) Ви повинні укладати його в квадратні дужки. Наприклад, `tcp://[fe80::1]:80`

> **Зауваження** :
> 
> Залежно від оточення, Unix-домени або довільний час очікування з'єднання можуть бути недоступними. Список доступних транспортів може бути отриманий за допомогою функції [stream\_get\_transports()](function.stream-get-transports.md). Дивіться список вбудованих транспортів на сторінці [Список підтримуваних транспортних протоколів](transports.md)

### Дивіться також

-   [stream\_socket\_server()](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.md) \- Встановити значення часу очікування потоку
-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fgetss()](function.fgetss.md) \- Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.md) \- Закриває відкритий дескриптор файлу
-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
-   [Опції cURL](ref.curl.md)
