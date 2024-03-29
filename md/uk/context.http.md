---
navigation:
  - context.socket.md: « Контекстні опції сокету
  - context.ftp.md: Параметри контексту FTP »
  - index.md: PHP Manual
  - context.md: Контекстні опції та параметри
title: Опції контексту HTTP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Опції контексту HTTP

Опції контексту HTTP — Список опцій контексту HTTP

### Опис

Опції контексту для транспортних протоколів `http://`и`https://`

### Опції

`method`string

**`GET`** **`POST`** або будь-який інший метод HTTP, який підтримує віддалений сервер.

По умолчанию\*\*`GET`\*\*

`header` array або string

Додаткові заголовки для надсилання разом із запитом. Значення в цій опції перевизначатимуть інші значення (такі як `User-agent:` `Host:`и`Authentication:`), даже при следующих переадресациях`Location:`Таким образом, не рекомендуется устанавливать заголовок`Host:`, якщо увімкнено параметр `follow_location`

`user_agent`string

Значення для надсилання разом із заголовком `User-Agent:`. Це значення буде використовуватися, якщо заголовок user-agent *не* був вказаний у опції контексту `header` вище.

За замовчуванням використовується значення директиви [user\_agent](filesystem.configuration.md#ini.user-agent)из файла php.ini.

`content`string

Додаткові дані для надсилання після заголовків. Зазвичай використовується із запитами POST та PUT.

`proxy`string

URI, що вказує на адресу проксі-сервера. (Наприклад, `tcp://proxy.example.com:5100`

`request_fulluri`bool

Когда установлено в\*\*`true`\*\*, весь URI буде використаний для формування запиту. (Наприклад, `GET http://www.example.com/path/to/file.md HTTP/1.0`). Хоча це нестандартний формат запиту, деякі проксі сервери вимагають його.

По умолчанию\*\*`false`\*\*

`follow_location`int

Наслідувати переадресації заголовка `Location`Для отключения установите в значение

По умолчанию

`max_redirects`int

Максимальна кількість переадресацій, якою можна слідувати. Значення або менше означає, що жодних переадресацій не буде зроблено.

По умолчанию`20`

`protocol_version`float

Версія протоколу HTTP.

По умолчанию`1.1`, починаючи з PHP 8.0.0; до цієї версії значення за промовчанням було `1.0`

`timeout`float

Час очікування на читання в секундах, вказаний у вигляді числа з плаваючою точкою (float), наприклад, `10.5`

За замовчуванням використовується значення директиви [default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)из файла php.ini.

`ignore_errors`bool

Витягти вміст навіть при неуспішних статусах завершення.

По умолчанию\*\*`false`\*\*

### Приклади

**Приклад #1 Вийняти сторінку та надіслати дані методом POST**

```php
<?php

$postdata = http_build_query(
    array(
        'var1' => 'некоторое содержимое',
        'var2' => 'doh'
    )
);

$opts = array('http' =>
    array(
        'method'  => 'POST',
        'header'  => 'Content-type: application/x-www-form-urlencoded',
        'content' => $postdata
    )
);

$context = stream_context_create($opts);

$result = file_get_contents('http://example.com/submit.php', false, $context);

?>
```

**Приклад #2 Ігнорувати переадресації, але витягти заголовки та вміст**

```php
<?php

$url = "http://www.example.org/header.php";

$opts = array('http' =>
    array(
        'method' => 'GET',
        'max_redirects' => '0',
        'ignore_errors' => '1'
    )
);

$context = stream_context_create($opts);
$stream = fopen($url, 'r', false, $context);

// информация о заголовках, а также
// метаданные о потоке
var_dump(stream_get_meta_data($stream));

// актуальная информация по ссылке $url
var_dump(stream_get_contents($stream));
fclose($stream);
?>
```

### Примітки

> **Зауваження** **Опції контексту нижчого потоку в сокеті**  
> Додаткові опції контексту можуть підтримуватись [нижчим транспортним протоколом](transports.inet.md). Для потоків `http://`, це стосується опцій контексту для транспортного протоколу `tcp://`. Для потоків `https://`, це стосується опцій контексту для транспортного протоколу `ssl://`

> **Зауваження** **Рядок статусу HTTP**  
> Коли ця обгортка потоку слідує за переадресацією, `wrapper_data`, що повертається функцією [stream\_get\_meta\_data()](function.stream-get-meta-data.md), необов'язково містить рядок статусу HTTP, який насправді відноситься до змісту даних за індексом
> 
> ```
> array (
>   'wrapper_data' =>
>   array (
>     0 => 'HTTP/1.0 301 Moved Permanently',
>     1 => 'Cache-Control: no-cache',
>     2 => 'Connection: close',
>     3 => 'Location: http://example.com/foo.jpg',
>     4 => 'HTTP/1.1 200 OK',
>     ...
> ```
> 
> Перший запит повернув код `301` (постійне перенаправлення), так що обгортка потоку автоматично послідувала цьому перенаправленню, щоб отримати відповідь `200`(индекс = `4`

### Дивіться також

-   [http://](wrappers.http.md)
-   [Контекстні опції сокету](context.socket.md)
-   [Опції контексту SSL](context.ssl.md)
