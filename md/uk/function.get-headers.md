- [«base64_encode](function.base64-encode.md)
- [get_meta_tags »](function.get-meta-tags.md)

- [PHP Manual](index.md)
- [Функції URL](ref.url.md)
- Повертає всі заголовки з відповіді сервера на запит HTTP

#get_headers

(PHP 5, PHP 7, PHP 8)

get_headers — Повертає всі заголовки з відповіді сервера на запит HTTP

### Опис

**get_headers**(string `$url`, bool `$associative` = **`false`**,
?resource `$context` = **`null`**): array\|false

**get_headers()** повертає масив із заголовками з відповіді сервера на
HTTP-запит.

### Список параметрів

`url`
Цільовий URL.

`associative`
Якщо необов'язковий параметр `associative` встановлено в ненульове
значення, **get_headers()** розбере відповідь сервера та встановить ключі для
повертається масиву.

`context`
Коректний контекст ресурсу, створений за допомогою
[stream_context_create()](function.stream-context-create.md) або
**`null`**, щоб використати контекст ресурсу за замовчуванням.

### Значення, що повертаються

Повертає індексований або асоціативний масив із заголовками відповіді
або **`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                     |
|--------|------------------------------------------------------------------------------------------|
| 8.0.0  | Тип параметра associative був змінений із цілого числа (int) на логічне значення (bool). |
| 7.1.0  | Доданий параметр context.                                                                |

### Приклади

**Приклад #1 Приклад використання **get_headers()****

` <?php$url = 'http://www.example.com';print_r(get_headers($url));print_r(get_headers($url, true));?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => HTTP/1.1 200 ОК
[1] => Дата: Sat, 29 May 2004 12:28:13 GMT
[2] => Server: Apache/1.3.27 (Unix) (Red-Hat/Linux)
[3] => Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
[4] => ETag: "3f80f-1b6-3e1cb03b"
[5] => Accept-Ranges: bytes
[6] => Content-Length: 438
[7] => Connection: close
[8] => Content-Type: text/html
)

Array
(
[0] => HTTP/1.1 200 ОК
[Date] => Sat, 29 May 2004 12:28:14 GMT
[Server] => Apache/1.3.27 (Unix) (Red-Hat/Linux)
[Last-Modified] => Wed, 08 Jan 2003 23:11:55 GMT
[ETag] => "3f80f-1b6-3e1cb03b"
[Accept-Ranges] => bytes
[Content-Length] => 438
[Connection] => close
[Content-Type] => text/html
)

**Приклад #2 Приклад використання запиту HEAD в
функції**get_headers()****

`<?php// За мовчанням функція get_headers використовує GET-запит для отримання заголовків. Если// вы хотите вместо него отправить HEAD-запрос, то это можно сделать, используя контекста потока:stream_context_set_default(    array(        'http' => array(            'method' => 'HEAD'        )    ));$headers = get_headers(' http://example.com');?> `

### Дивіться також

- [apache_request_headers()](function.apache-request-headers.md) -
Отримує список усіх заголовків HTTP-запиту
