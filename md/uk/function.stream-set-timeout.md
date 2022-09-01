---
navigation:
  - function.stream-set-read-buffer.html: « streamsetreadbuffer
  - function.stream-set-write-buffer.html: streamsetwritebuffer »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsettimeout
---
# streamsettimeout

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamsettimeout — Встановлення часу очікування потоку.

### Опис

```methodsynopsis
stream_set_timeout(resource $stream, int $seconds, int $microseconds = 0): bool
```

Встановлює значення часу очікування у потоці `stream`, що дорівнює сумі параметрів `seconds` і `microseconds`

Коли час роботи потоку спливає, ключ 'timedout' масиву, що повертається функцією [streamgetmetadata()](function.stream-get-meta-data.html), встановлюється в значення \*\*`true`\*\*хоча помилка або попередження не генерується.

### Список параметрів

`stream`

Цільовий потік.

`seconds`

Секунди в установленому часі очікування.

`microseconds`

Мікросекунди в установленому часі очікування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **streamsettimeout()****

```php
<?php
$fp = fsockopen("www.example.com", 80);
if (!$fp) {
    echo "Невозможно открыть сокет\n";
} else {

    fwrite($fp, "GET / HTTP/1.0\r\n\r\n");
    stream_set_timeout($fp, 2);
    $res = fread($fp, 2000);

    $info = stream_get_meta_data($fp);
    fclose($fp);

    if ($info['timed_out']) {
        echo 'Истекло время соединения!';
    } else {
        echo $res;
    }

}
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не працює з просунутими операціями, такими як [streamsocketrecvfrom()](function.stream-socket-recvfrom.html). Використовуйте замість неї [streamselect()](function.stream-select.html) з параметром часу очікування.

Ця функція раніше викликалася через **setsockettimeout()** і пізніше через [socketsettimeout()](function.socket-set-timeout.html)але це використання застаріло.

### Дивіться також

-   [fsockopen()](function.fsockopen.md) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [fopen()](function.fopen.md) - Відкриває файл або URL
