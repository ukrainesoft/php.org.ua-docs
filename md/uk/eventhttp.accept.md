---
navigation:
  - class.eventhttp.md: « EventHttp
  - eventhttp.addserveralias.md: 'EventHttp::addServerAlias »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::accept'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttp::accept

(PECL event >= 1.2.6-beta)

EventHttp::accept — Примушує HTTP-сервер приймати з'єднання із зазначеним потоком сокету або ресурсом

### Опис

```methodsynopsis
public
   EventHttp::accept(
    mixed
     $socket
   ): bool
```

Примушує HTTP-сервер приймати з'єднання із зазначеним потоком сокету чи ресурсом. Сокет повинен бути готовим до прийому з'єднань.

Може викликатись кілька разів, щоб приймати з'єднання на різних сокетах.

> **Зауваження** :
> 
> Щоб зв'язати сокет, `прослухати`и`прийняти` з'єднання на сокеті в одному дзвінку, використовуйте [EventHttp::bind()](eventhttp.bind.md). . **EventHttp::accept()** потрібно лише в тому випадку, якщо один виклик вже має сокет, готовий для прийняття з'єднань.

### Список параметрів

`socket`

Ресурс сокету, потоковий або числовий дескриптор файлу, що представляє сокет, готовий приймати з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**EventHttp::accept()\*\*\*\*

```php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$addresses = array (
     8091 => "127.0.0.1",
     8092 => "127.0.0.2",
);
$i = 0;

$socket = array();

foreach ($addresses as $port => $ip) {
    echo $ip, " ", $port, PHP_EOL;
    $socket[$i] = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
    if (!socket_bind($socket[$i], $ip, $port)) {
        exit("ошибка socket_bind\n");
    }
    socket_listen($socket[$i], 0);
    socket_set_nonblock($socket[$i]);

    if (!$http->accept($socket[$i])) {
        echo "Принять не удалось\n";
        exit(1);
    }

    ++$i;
}

$http->setCallback("/some-page", function() {
 echo "(some-page)\n";
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$http->setDefaultCallback(function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$signal = Event::signal($base, SIGINT, function () use ($base) {
    echo "Пойман SIGINT. Останавливаем...\n";
    $base->stop();
});
$signal->add();

$base->dispatch();
echo "конец\n";
// Мы не закрывали сокеты, так как Libevent
// уже установил флаги CLOSE_ON_FREE и CLOSE_ON_EXEC
// в дескрипторе файла, связанном с сокетами.
?>
```

Висновок наведеного прикладу буде схожим на:

```
Client:
$ nc 127.0.0.1 8091
GET /about HTTP/1.0
Connection: close

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close

Server:
127.0.0.1 8091
127.0.0.2 8092
URI: /about
OK
```

### Дивіться також

-   [EventHttp::bind()](eventhttp.bind.md) \- Прив'язує HTTP-сервер до вказаної адреси та порту
