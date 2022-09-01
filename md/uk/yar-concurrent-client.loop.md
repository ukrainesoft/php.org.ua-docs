---
navigation:
  - yar-concurrent-client.call.html: '« YarConcurrentClient::call'
  - yar-concurrent-client.reset.html: 'YarConcurrentClient::reset »'
  - index.md: PHP Manual
  - class.yar-concurrent-client.html: YarConcurrentClient
title: 'YarConcurrentClient::loop'
---
# YarConcurrentClient::loop

(PECL yar >= 1.0.0)

YarConcurrentClient::loop — Запуск усіх зареєстрованих дзвінків

### Опис

```methodsynopsis
public static Yar_Concurrent_Client::loop(callable $callback = ?, callable $error_callback = ?): bool
```

Запускає всі зареєстровані дзвінки.

### Список параметрів

`callback`

Якщо задана функція зворотного дзвінка, то вона буде запущена після запуску всіх запитів, але до отримання відповідей від них з $callinfo рівним NULL.

Далі, якщо функція зворотного дзвінка не була задана під час реєстрації дзвінка, то для обробки результату буде викликана ця функція.

`error_callback`

Якщо цей параметр заданий, Yar запустить цю функцію у разі виникнення помилки.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YarConcurrentClient::loop()****

```php
<?php
function callback($retval, $callinfo) {
     if ($callinfo == NULL) {
        echo "Так, все запросы запущены, но пока ни одного ответа\n";
     } else {
        echo "Это ответ от удалённого запроса. Имя метода", $callinfo["method"],
             ". Был зарегистрирован " , $callinfo["sequence"] , "\n";
        var_dump($retval);
     }
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

Yar_Concurrent_Client::loop("callback", "error_callback"); //запускаем запросы,
                                                           //параметр error_callback не обязателен
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Так, все запросы запущены, но пока ни одного ответа
Это ответ от удалённого запроса. Имя метода issome_method. Был зарегистрирован 4
string(11) "some_method"
Это ответ от удалённого запроса. Имя метода issome_method. Был зарегистрирован 1
string(11) "some_method"
Это ответ от удалённого запроса. Имя метода issome_method. Был зарегистрирован 2
string(11) "some_method"
Это ответ от удалённого запроса. Имя метода issome_method. Был зарегистрирован 3
string(11) "some_method"
```

### Дивіться також

-   [YarConcurrentClient::call()](yar-concurrent-client.call.html) - Зареєструвати конкурентний виклик
-   [YarConcurrentClient::reset()](yar-concurrent-client.reset.html) - Очистити всі зареєстровані дзвінки
-   [YarServer::construct()](yar-server.construct.html) - Конструктор YarServer
-   [YarServer::handle()](yar-server.handle.html) - Запустити сервер RPC
