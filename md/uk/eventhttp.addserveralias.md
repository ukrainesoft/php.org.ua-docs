Додає псевдонім сервера до об'єкта HTTP-сервера

-   [« EventHttp::accept](eventhttp.accept.html)
    
-   [EventHttp::bind »](eventhttp.bind.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttp](class.eventhttp.html)
    
-   Додає псевдонім сервера до об'єкта HTTP-сервера
    

# EventHttp::addServerAlias

(PECL event >= 1.4.0-beta)

EventHttp::addServerAlias ​​— Додає псевдонім сервера до об'єкта HTTP-сервера

### Опис

```methodsynopsis
public
   EventHttp::addServerAlias(
    string
     $alias
   ): bool
```

Додає псевдонім сервера до об'єкта сервера HTTP.

### Список параметрів

`alias`

Псевдонім для додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventHttp::addServerAlias()****

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) ошибка\n");
};

if (!$http->addServerAlias("local.net")) {
    exit("Не удалось добавить псевдоним сервера\n");
}

$http->setCallback("/about", function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});
$base->dispatch();
?>
```

### Дивіться також

-   [EventHttp::removeServerAlias()](eventhttp.removeserveralias.html) - Видаляє псевдонім сервера