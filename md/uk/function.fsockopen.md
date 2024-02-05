---
navigation:
  - function.dns-get-record.md: « dns\_get\_record
  - function.gethostbyaddr.md: gethostbyaddr »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: fsockopen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fsockopen

(PHP 4, PHP 5, PHP 7, PHP 8)

fsockopen — Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix

### Опис

```methodsynopsis
fsockopen(    string $hostname,    int $port = -1,    int &$error_code = null,    string &$error_message = null,    ?float $timeout = null): resource|false
```

Устанавливает соединение с сокетом ресурса`hostname`

PHP підтримує цільові ресурси в інтернеті та Unix-доменах у тому вигляді, як вони описані в [Список підтримуваних транспортних протоколів](transports.md). Список підтримуваних транспортів можна отримати за допомогою функції [stream\_get\_transports()](function.stream-get-transports.md)

За умовчанням сокет буде відкритий у режимі блокування. Переключити його в неблокуючий режим можна функцією [stream\_set\_blocking()](function.stream-set-blocking.md)

[stream\_socket\_client()](function.stream-socket-client.md) виконує аналогічну функцію, але надає ширший вибір налаштувань з'єднання, що включає встановлення неблокуючого режиму та можливість надання потокового контексту.

### Список параметрів

`hostname`

Якщо [встановлена](openssl.installation.md) Підтримка OpenSSL, можна використовувати SSL або TLS-протоколи з'єднань поверх TCP/IP при підключенні до віддаленого хоста. Для цього перед `hostname`нужно добавить префикс`ssl://`или`tls://`

`port`

Номер порту. Його можна не вказувати, передавши `-1` для тих протоколів, які не використовують порти, наприклад `unix://`

`error_code`

Якщо цей параметр надати, у разі виникнення помилки системного виклику функції `connect()` він прийматиме номер цієї помилки.

Если значение параметра`error_code` одно , а функція повернула **`false`**, отже помилка сталася до виклику `connect()`. Найчастіше це свідчить про проблеми при ініціалізації сокету.

`error_message`

Повідомлення про помилку у вигляді рядка.

`timeout`

Время ожидания соединения в секундах. Если\*\*`null`\*\*, використовується налаштування php.ini [default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)

> **Зауваження** :
> 
> Якщо потрібно встановити час очікування/запису даних через сокет, використовуйте функцію [stream\_set\_timeout()](function.stream-set-timeout.md), т.к. параметр`timeout` функції **fsockopen()** обмежує лише час процесу встановлення з'єднання із сокетом.

### Значення, що повертаються

**fsockopen()** повертає файловий покажчик, який можна використовувати з функціями, що працюють із файлами (такі як [fgets()](function.fgets.md) [fgetss()](function.fgetss.md) [fwrite()](function.fwrite.md) [fclose()](function.fclose.md) і [feof()](function.feof.md)). Якщо дзвінок завершиться невдало, функція поверне **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо `hostname` не є допустимим доменом.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timeout` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**fsockopen()\*\*\*\*

```php
<?php
$fp = fsockopen("www.example.com", 80, $errno, $errstr, 30);
if (!$fp) {
    echo "$errstr ($errno)<br />\n";
} else {
    $out = "GET / HTTP/1.1\r\n";
    $out .= "Host: www.example.com\r\n";
    $out .= "Connection: Close\r\n\r\n";
    fwrite($fp, $out);
    while (!feof($fp)) {
        echo fgets($fp, 128);
    }
    fclose($fp);
}
?>
```

**Приклад #2 Використання UDP-з'єднання**

Приклад нижче демонструє, як отримати день та час від UDP-служби "daytime" (порт 13) на машині.

```php
<?php
$fp = fsockopen("udp://127.0.0.1", 13, $errno, $errstr);
if (!$fp) {
    echo "ERROR: $errno - $errstr<br />\n";
} else {
    fwrite($fp, "\n");
    echo fread($fp, 26);
    fclose($fp);
}
?>
```

### Примітки

> **Зауваження** :
> 
> Залежно від оточення, домену Unix або часу очікування встановлення підключення може бути недоступним.

**Увага**

Іноді UDP-сокети набувають статусу відкритих, навіть якщо віддалений хост недоступний. Помилка проявить себе тільки під час читання або запису даних з цього сокету. Причина цього полягає в тому, що протокол UDP передає дані без встановлення з'єднання, а це означає, що операційна система не встановлює та не тримає з'єднання із сокетом, доки не почнеться передача даних.

> **Зауваження**: Якщо вказати числову адресу IPv6 (наприклад, `fe80::1`) Ви повинні укладати його в квадратні дужки. Наприклад, `tcp://[fe80::1]:80`

### Дивіться також

-   [pfsockopen()](function.pfsockopen.md) \- Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_socket\_client()](function.stream-socket-client.md) \- Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.md) \- Встановити значення часу очікування потоку
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fgetss()](function.fgetss.md) \- Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.md) \- Закриває відкритий дескриптор файлу
-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [Модуль Curl](ref.curl.md)
