---
navigation:
  - eventhttp.accept.md: '« EventHttp::accept'
  - eventhttp.bind.md: 'EventHttp::bind »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::addServerAlias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**EventHttp::addServerAlias()\*\*\*\*

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) ошибка\n");
};

if (!$http->addServerAlias("local.net")) {
    exit("Не удалось добавить псевдоним сервера\n");
}

$http->setCallback("/about", function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});
$base->dispatch();
?>
```

### Дивіться також

-   [EventHttp::removeServerAlias()](eventhttp.removeserveralias.md) \- Видаляє псевдонім сервера
