Виклик сервісу

-   [« YarClient](class.yar-client.html)
    
-   [YarClient::construct »](yar-client.construct.html)
    
-   [PHP Manual](index.html)
    
-   [YarClient](class.yar-client.html)
    
-   Виклик сервісу
    

# YarClient::call

(PECL yar >= 1.0.0)

YarClient::call — Виклик сервісу

### Опис

```methodsynopsis
public Yar_Client::__call(string $method, array $parameters): void
```

Здійснює виклик віддаленого RPC-метода.

### Список параметрів

`method`

Ім'я дистанційного методу.

`parameters`

Параметри.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YarClient::call()****

```php
<?php

$client = new Yar_Client("http://host/api/");

/* вызов удалённого сервиса */
$result = $client->some_method("parameter");
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarClient::setOpt()](yar-client.setopt.html) - Задати контекст виклику