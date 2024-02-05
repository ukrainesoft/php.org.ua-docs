---
navigation:
  - class.yar-concurrent-client.md: « Yar\_Concurrent\_Client
  - yar-concurrent-client.loop.md: 'Yar\_Concurrent\_Client::loop »'
  - index.md: PHP Manual
  - class.yar-concurrent-client.md: Yar\_Concurrent\_Client
title: 'Yar\_Concurrent\_Client::call'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Concurrent\_Client::call

(PECL yar >= 1.0.0)

Yar\_Concurrent\_Client::call — Зареєструвати конкурентний виклик

### Опис

```methodsynopsis
public static Yar_Concurrent_Client::call(    string $uri,    string $method,    array $parameters = ?,    callable $callback = ?,    callable $error_callback = ?,    array $options = ?): int
```

Реєструє RPC-дзвінок, але не надсилає його негайно, а відкладає до моменту виклику [Yar\_Concurrent\_Client::loop()](yar-concurrent-client.loop.md)

### Список параметрів

`uri`

URI (http, tcp) сервера RPC

`method`

Ім'я сервісу (ім'я методу)

`parameters`

Параметри

`callback`

Callback-функція, яка буде викликана після відпрацювання віддаленого запиту.

### Значення, що повертаються

Унікальний ідентифікатор.

### Приклади

**Приклад #1 Приклад використання** Yar\_Concurrent\_Client::call()\*\*\*\*

```php
<?php
function callback($retval, $callinfo) {
     var_dump($retval);
}

function error_callback($type, $error, $callinfo) {
    error_log($error);
}

Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback");

//если функция обратного вызова не задана, то будет использована определённая в цикле вызовов
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"));

//этот сервер принимает упаковку JSON
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_PACKAGER => "json"));

//отдельно заданное время ожидания
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_TIMEOUT=>1));

//запросы всё ещё не запущены
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Concurrent\_Client::loop()](yar-concurrent-client.loop.md) \- Запуск усіх зареєстрованих викликів
-   [Yar\_Concurrent\_Client::reset()](yar-concurrent-client.reset.md) \- Очистити всі зареєстровані дзвінки
-   [Yar\_Server::\_\_construct()](yar-server.construct.md) \- Конструктор Yar\_Server
-   [Yar\_Server::handle()](yar-server.handle.md) \- Запустити сервер RPC
