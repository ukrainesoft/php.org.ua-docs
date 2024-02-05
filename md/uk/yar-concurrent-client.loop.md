---
navigation:
  - yar-concurrent-client.call.md: '« Yar\_Concurrent\_Client::call'
  - yar-concurrent-client.reset.md: 'Yar\_Concurrent\_Client::reset »'
  - index.md: PHP Manual
  - class.yar-concurrent-client.md: Yar\_Concurrent\_Client
title: 'Yar\_Concurrent\_Client::loop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Concurrent\_Client::loop

(PECL yar >= 1.0.0)

Yar\_Concurrent\_Client::loop — Запуск усіх зареєстрованих дзвінків

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

**Пример #1 Пример использования**Yar\_Concurrent\_Client::loop()\*\*\*\*

```php
<?php
function callback($retval, $callinfo) {
     if ($callinfo == NULL) {
        echo "Так, все запросы запущены, но пока ни одного ответа\n";
     } else {
        echo "Это ответ от удалённого запроса. Имя метода", $callinfo["method"],
             ". Был зарегистрирован " , $callinfo["sequence"] , "\n";
        var_dump($retval);
     }
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

Yar_Concurrent_Client::loop("callback", "error_callback"); //запускаем запросы,
                                                           //параметр error_callback не обязателен
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [Yar\_Concurrent\_Client::call()](yar-concurrent-client.call.md) \- Зареєструвати конкурентний виклик
-   [Yar\_Concurrent\_Client::reset()](yar-concurrent-client.reset.md) \- Очистити всі зареєстровані дзвінки
-   [Yar\_Server::\_\_construct()](yar-server.construct.md) \- Конструктор Yar\_Server
-   [Yar\_Server::handle()](yar-server.handle.md) \- Запустити сервер RPC
