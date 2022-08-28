Конструктор YarClient

-   [« Yar\_Client::\_\_call](yar-client.call.html)
    
-   [Yar\_Client::setOpt »](yar-client.setopt.html)
    
-   [PHP Manual](index.html)
    
-   [Yar\_Client](class.yar-client.html)
    
-   Конструктор YarClient
    

# YarClient::construct

(PECL yar >= 1.0.0)

YarClient::construct — Конструктор YarClient

### Опис

```methodsynopsis
final public Yar_Client::__construct(string $url, array $options = ?)
```

Створює [Yar\_Client](class.yar-client.html) для [Yar\_Server](class.yar-server.html)

### Список параметрів

`url`

URL сервера Yar.

### Значення, що повертаються

Об'єкт класу [Yar\_Client](class.yar-client.html)

### Приклади

**Приклад #1 Приклад використання **YarClient::construct()****

```php
<?php
$client = new Yar_Client("http://host/api/");
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [Yar\_Client::\_\_call()](yar-client.call.html) - Виклик сервісу
-   [Yar\_Client::setOpt()](yar-client.setopt.html) - Задати контекст виклику