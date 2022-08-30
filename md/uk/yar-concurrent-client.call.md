Зареєструвати конкурентний виклик

-   [« YarConcurrentClient](class.yar-concurrent-client.html)
    
-   [YarConcurrentClient::loop »](yar-concurrent-client.loop.html)
    
-   [PHP Manual](index.html)
    
-   [YarConcurrentClient](class.yar-concurrent-client.html)
    
-   Зареєструвати конкурентний виклик
    

# YarConcurrentClient::call

(PECL yar >= 1.0.0)

YarConcurrentClient::call — Зареєструвати конкурентний виклик

### Опис

```methodsynopsis
public static Yar_Concurrent_Client::call(    string $uri,    string $method,    array $parameters = ?,    callable $callback = ?,    callable $error_callback = ?,    array $options = ?): int
```

Реєструє RPC-дзвінок, але не надсилає його негайно, а відкладає до моменту виклику [YarConcurrentClient::loop()](yar-concurrent-client.loop.html)

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

**Приклад #1 Приклад використання **YarConcurrentClient::call()****

```php
<?php
function callback($retval, $callinfo) {
     var_dump($retval);
}

function error_callback($type, $error, $callinfo) {
    error_log($error);
}

Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback");

//если функция обратного вызова не задана, то будет использована определённая в цикле вызовов
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"));

//этот сервер принимает упаковку JSON
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_PACKAGER => "json"));

//отдельно заданное время ожидания
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_TIMEOUT=>1));

//запросы всё ещё не запущены
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarConcurrentClient::loop()](yar-concurrent-client.loop.html) - Запуск усіх зареєстрованих викликів
-   [YarConcurrentClient::reset()](yar-concurrent-client.reset.html) - Очистити всі зареєстровані дзвінки
-   [YarServer::construct()](yar-server.construct.html) - Конструктор YarServer
-   [YarServer::handle()](yar-server.handle.html) - Запустити сервер RPC