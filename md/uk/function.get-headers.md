---
navigation:
  - function.base64-encode.md: « base64\_encode
  - function.get-meta-tags.md: get\_meta\_tags »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: get\_headers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_headers

(PHP 5, PHP 7, PHP 8)

get\_headers — Повертає всі заголовки з відповіді сервера на запит HTTP

### Опис

```methodsynopsis
get_headers(string $url, bool $associative = false, ?resource $context = null): array|false
```

**get\_headers()** повертає масив із заголовками із відповіді сервера на HTTP-запит.

### Список параметрів

`url`

Цільовий URL.

`associative`

Якщо необов'язковий параметр `associative`установлен в ненулевое значение,**get\_headers()** розбере відповідь сервера і встановить ключі для масиву, що повертається.

`context`

Коректний контекст ресурсу, створений за допомогою [stream\_context\_create()](function.stream-context-create.md)или\*\*`null`\*\*, щоб використовувати контекст за замовчуванням.

### Значення, що повертаються

Повертає індексований або асоціативний масив із заголовками відповіді або \*\*`false`\*\*при возникновении ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тип параметра `associative` був змінений із цілого числа (int) на логічне значення (bool). |
| 7.1.0 | Добавлен параметр`context` |

### Приклади

**Приклад #1 Приклад використання** get\_headers()\*\*\*\*

```php
<?php
$url = 'http://www.example.com';

print_r(get_headers($url));

print_r(get_headers($url, true));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => HTTP/1.1 200 OK
    [1] => Date: Sat, 29 May 2004 12:28:13 GMT
    [2] => Server: Apache/1.3.27 (Unix)  (Red-Hat/Linux)
    [3] => Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
    [4] => ETag: "3f80f-1b6-3e1cb03b"
    [5] => Accept-Ranges: bytes
    [6] => Content-Length: 438
    [7] => Connection: close
    [8] => Content-Type: text/html
)

Array
(
    [0] => HTTP/1.1 200 OK
    [Date] => Sat, 29 May 2004 12:28:14 GMT
    [Server] => Apache/1.3.27 (Unix)  (Red-Hat/Linux)
    [Last-Modified] => Wed, 08 Jan 2003 23:11:55 GMT
    [ETag] => "3f80f-1b6-3e1cb03b"
    [Accept-Ranges] => bytes
    [Content-Length] => 438
    [Connection] => close
    [Content-Type] => text/html
)
```

**Приклад #2 Приклад використання запиту HEAD у функції**get\_headers()\*\*\*\*

```php
<?php
// По умолчанию функция get_headers использует GET-запрос для получения заголовков. Если
// вы хотите вместо него отправить HEAD-запрос, то это можно сделать, используя контекста потока:
$context = stream_context_create(
    [
        'http' => array(
            'method' => 'HEAD'
        )
    ]
);
$headers = get_headers('http://example.com', false, $context);
?>
```

### Дивіться також

-   [apache\_request\_headers()](function.apache-request-headers.md) \- Отримує список усіх заголовків HTTP-запиту
