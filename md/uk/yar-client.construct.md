Конструктор YarClient

-   [« YarClient::call](yar-client.call.html)
    
-   [YarClient::setOpt »](yar-client.setopt.html)
    
-   [PHP Manual](index.html)
    
-   [YarClient](class.yar-client.html)
    
-   Конструктор YarClient
    

# YarClient::construct

(PECL yar >= 1.0.0)

YarClient::construct — Конструктор YarClient

### Опис

```methodsynopsis
final public Yar_Client::__construct(string $url, array $options = ?)
```

Створює [YarClient](class.yar-client.html) для [YarServer](class.yar-server.html)

### Список параметрів

`url`

URL сервера Yar.

### Значення, що повертаються

Об'єкт класу [YarClient](class.yar-client.html)

### Приклади

**Приклад #1 Приклад використання **YarClient::construct()****

```php
<?php
$client = new Yar_Client("http://host/api/");
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarClient::call()](yar-client.call.html) - Виклик сервісу
-   [YarClient::setOpt()](yar-client.setopt.html) - Задати контекст виклику