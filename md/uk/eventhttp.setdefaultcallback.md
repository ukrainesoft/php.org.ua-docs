Встановлює callback-функцію за промовчанням для обробки запитів, які не перехоплюються конкретними callback-функціями

-   [« EventHttp::setCallback](eventhttp.setcallback.html)
    
-   [EventHttp::setMaxBodySize »](eventhttp.setmaxbodysize.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttp](class.eventhttp.html)
    
-   Встановлює callback-функцію за промовчанням для обробки запитів, які не перехоплюються конкретними callback-функціями
    

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

Callback-функція [callable](language.types.callable.html). Повинна відповідати наступному прототипу:

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

Об'єкт [EventHttpRequest](class.eventhttprequest.html)

`arg`

Дані користувача.

`arg`

Користувальницькі дані, що передаються в callback-функцію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventHttp::setDefaultCallback()****

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) failed\n");
};

$http->setDefaultCallback(function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});

$base->dispatch();
?>
```

### Дивіться також

-   [EventHttp::setCallback()](eventhttp.setcallback.html) - Встановлює callback-функцію для зазначеного URI