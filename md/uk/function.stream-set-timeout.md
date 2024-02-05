---
navigation:
  - function.stream-set-read-buffer.md: « stream\_set\_read\_buffer
  - function.stream-set-write-buffer.md: stream\_set\_write\_buffer »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_set\_timeout
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_set\_timeout

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_set\_timeout — Встановлення часу очікування потоку.

### Опис

```methodsynopsis
stream_set_timeout(resource $stream, int $seconds, int $microseconds = 0): bool
```

Устанавливает значение времени ожидания в потоке`stream`, равное сумме параметров`seconds`и`microseconds`

Коли час роботи потоку спливає, ключ 'timed\_out' масиву, що повертається функцією [stream\_get\_meta\_data()](function.stream-get-meta-data.md), устанавливается в значение\*\*`true`\*\*хоча помилка або попередження не генерується.

### Список параметрів

`stream`

Цільовий потік.

`seconds`

Секунди в установленому часі очікування.

`microseconds`

Мікросекунди в установленому часі очікування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** stream\_set\_timeout()\*\*\*\*

```php
<?php
$fp = fsockopen("www.example.com", 80);
if (!$fp) {
    echo "Невозможно открыть сокет\n";
} else {

    fwrite($fp, "GET / HTTP/1.0\r\n\r\n");
    stream_set_timeout($fp, 2);
    $res = fread($fp, 2000);

    $info = stream_get_meta_data($fp);
    fclose($fp);

    if ($info['timed_out']) {
        echo 'Истекло время соединения!';
    } else {
        echo $res;
    }

}
?>
```

### Примітки

> **Зауваження** :
> 
> Ця функція не працює з просунутими операціями, такими як [stream\_socket\_recvfrom()](function.stream-socket-recvfrom.md). Використовуйте замість неї [stream\_select()](function.stream-select.md)с параметром времени ожидания.

Ця функція раніше викликалася через **set\_socket\_timeout()** і пізніше через [socket\_set\_timeout()](function.socket-set-timeout.md)але це використання застаріло.

### Дивіться також

-   [fsockopen()](function.fsockopen.md) \- Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
