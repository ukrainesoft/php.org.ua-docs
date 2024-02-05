---
navigation:
  - eventhttp.setcallback.md: '« EventHttp::setCallback'
  - eventhttp.setmaxbodysize.md: 'EventHttp::setMaxBodySize »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::setDefaultCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttp::setDefaultCallback

(PECL event >= 1.4.0-beta)

EventHttp::setDefaultCallback — Встановлює стандартну callback-функцію для обробки запитів, які не перехоплюються конкретними callback-функціями

### Опис

```methodsynopsis
public
   EventHttp::setDefaultCallback(
    string
     $cb
   , 
    string
     $arg
    = ?): void
```

Встановлює callback-функцію за промовчанням для обробки запитів, які не перехоплюються конкретними callback-функціями

### Список параметрів

`cb`

Callback-функция[callable](language.types.callable.md). Повинна відповідати наступному прототипу:

```methodsynopsis
callback(
       EventHttpRequest
        $req
        = NULL
      , 
       mixed
        $arg
        = NULL
      ): void
```

`req`

Об'єкт [EventHttpRequest](class.eventhttprequest.md)

`arg`

Дані користувача.

`arg`

Користувальницькі дані, що передаються в callback-функцію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**EventHttp::setDefaultCallback()\*\*\*\*

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) failed\n");
};

$http->setDefaultCallback(function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});

$base->dispatch();
?>
```

### Дивіться також

-   [EventHttp::setCallback()](eventhttp.setcallback.md) \- Встановлює callback-функцію для зазначеного URI
