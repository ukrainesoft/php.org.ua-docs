---
navigation:
  - eventhttp.addserveralias.md: '« EventHttp::addServerAlias'
  - eventhttp.construct.md: 'EventHttp::\_\_construct »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttp::bind

(PECL event >= 1.2.6-beta)

EventHttp::bind — Прив'язує HTTP-сервер до вказаної адреси та порту

### Опис

```methodsynopsis
public
   EventHttp::bind(
    string
     $address
   , 
    int
     $port
   ): void
```

Прив'язує HTTP-сервер до вказаної адреси та порту.

Може викликатися кілька разів для прив'язки того самого HTTP-сервера до кількох різних портів.

### Список параметрів

`address`

Рядок, що містить IP-адресу для `прослуховування(2)`

`port`

Номер порту для прослуховування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** EventHttp::bind()\*\*\*\*

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("связать(1) не удалось\n");
};
if (!$http->bind("127.0.0.1", 8089)) {
    exit("связать(2) не удалось\n");
};

$http->setCallback("/about", function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$base->dispatch();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Client:

$ nc 127.0.0.1 8088
GET /about HTTP/1.0
Connection: close

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close

$ nc 127.0.0.1 8089
GET /unknown HTTP/1.0
Connection: close

HTTP/1.1 404 Not Found
Content-Type: text/html
Date: Wed, 13 Mar 2013 04:14:41 GMT
Content-Length: 149
Connection: close

<html><head><title>404 Not Found</title></head><body><h1>Not Found</h1><p>The requested URL /unknown was not found on this server.</p></body></html>

Server:
URI: /about
OK
```

### Дивіться також

-   [EventHttp::accept()](eventhttp.accept.md) \- Примушує HTTP-сервер приймати з'єднання із зазначеним потоком сокету чи ресурсом
