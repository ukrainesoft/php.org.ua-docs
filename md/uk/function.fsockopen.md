---
navigation:
  - function.dns-get-record.md: « dnsgetrecord
  - function.gethostbyaddr.md: gethostbyaddr »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: fsockopen
---
# fsockopen

(PHP 4, PHP 5, PHP 7, PHP 8)

fsockopen — Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix

### Опис

```methodsynopsis
fsockopen(    string $hostname,    int $port = -1,    int &$error_code = null,    string &$error_message = null,    ?float $timeout = null): resource|false
```

Встановлює з'єднання із сокетом ресурсу `hostname`

PHP підтримує цільові ресурси в інтернеті та Unix-доменах у тому вигляді, як вони описані в [Список підтримуваних транспортних протоколів](transports.md). Список підтримуваних транспортів можна отримати за допомогою функції [streamgettransports()](function.stream-get-transports.md)

За замовчуванням сокет буде відкритий у режимі блокування. Переключити його в неблокуючий режим можна функцією [streamsetblocking()](function.stream-set-blocking.md)

[streamsocketclient()](function.stream-socket-client.md) виконує аналогічну функцію, але надає ширший вибір налаштувань з'єднання, що включає встановлення неблокуючого режиму та можливість надання потокового контексту.

### Список параметрів

`hostname`

Якщо [установлена](openssl.installation.md) Підтримка OpenSSL, можна використовувати SSL або TLS-протоколи з'єднань поверх TCP/IP при підключенні до віддаленого хоста. Для цього перед `hostname` потрібно додати префікс `ssl://` або `tls://`

`port`

Номер порту. Його можна не вказувати, передавши `-1` для тих протоколів, які не використовують порти, наприклад `unix://`

`error_code`

Якщо цей параметр надати, у разі виникнення помилки системного виклику функції `connect()` він прийматиме номер цієї помилки.

Якщо значення параметра `error_code` одно `0`, а функція повернула **`false`**, отже помилка сталася до виклику `connect()`. Найчастіше це свідчить про проблеми при ініціалізації сокету.

`error_message`

Повідомлення про помилку у вигляді рядка.

`timeout`

Час очікування з'єднання за секунди. Якщо **`null`**, використовується налаштування php.ini [defaultsockettimeout](filesystem.configuration.md#ini.default-socket-timeout)

> **Зауваження**
> 
> Якщо потрібно встановити час очікування/запису даних через сокет, використовуйте функцію [streamsettimeout()](function.stream-set-timeout.md), т.к. параметр `timeout` функції **fsockopen()** обмежує лише час процесу встановлення з'єднання із сокетом.

### Значення, що повертаються

**fsockopen()** повертає файловий покажчик, який можна використовувати з функціями, що працюють із файлами (такі як [fgets()](function.fgets.md) [fgetss()](function.fgetss.md) [fwrite()](function.fwrite.md) [fclose()](function.fclose.md) і [feof()](function.feof.md)). Якщо дзвінок завершиться невдало, функція поверне **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо `hostname` не є допустимим доменом.

### список змін

| Версия | Описание |
| --- | --- |
|  | `timeout` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **fsockopen()****

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

> **Зауваження**
> 
> Залежно від оточення, домену Unix або часу очікування встановлення підключення можуть виявитися недоступними.

**Увага**

Іноді UDP-сокети набувають статусу відкритих, навіть якщо віддалений хост недоступний. Помилка проявить себе лише під час читання або запису даних з цього сокету. Причина цього полягає в тому, що протокол UDP передає дані без встановлення з'єднання, а це означає, що операційна система не встановлює та не тримає з'єднання з сокетом, доки не почнеться передача даних.

> **Зауваження**: Якщо вказати числову адресу IPv6 (наприклад, `fe80::1`) Ви повинні укладати його в квадратні дужки. Наприклад, `tcp://[fe80::1]:80`

### Дивіться також

-   [pfsockopen()](function.pfsockopen.md) - Відкриває постійне з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [streamsocketclient()](function.stream-socket-client.md) - Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [streamsetblocking()](function.stream-set-blocking.md) - Встановити блокуючий/неблокуючий режим у потоці
-   [streamsettimeout()](function.stream-set-timeout.md) - Встановити значення часу очікування потоку
-   [fgets()](function.fgets.md) - Читає рядок із файлу
-   [fgetss()](function.fgetss.md) - Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.md) - Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.md) - Закриває відкритий дескриптор файлу
-   [feof()](function.feof.md) - Перевіряє, чи кінець файлу досягнуто
-   [socketconnect()](function.socket-connect.md) - Починає з'єднання із сокетом
-   [Модуль Curl](ref.curl.md)
