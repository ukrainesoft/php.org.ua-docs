Отримати тип виключення

-   [« YarServerException](class.yar-server-exception.html)
    
-   [YarClientException »](class.yar-client-exception.html)
    
-   [PHP Manual](index.md)
    
-   [YarServerException](class.yar-server-exception.html)
    
-   Отримати тип виключення
    

# YarServerException::getType

(PECL yar >= 1.0.0)

YarServerException::getType — Отримати тип виключення

### Опис

```methodsynopsis
public Yar_Server_Exception::getType(): string
```

Отримати початковий виняток, викинутий на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок

### Приклади

**Приклад #1 Приклад використання **YarServerException::getType()****

```php
//Server.php
<?php
class Custom_Exception extends Exception {};

class API {
    public function throw_exception($name) {
        throw new Custom_Exception($name);
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>

//Client.php
<?php
$client = new Yar_Client("http://host/api.php");

try {
    $client->throw_exception("client");
} catch (Yar_Server_Exception $e) {
    var_dump($e->getType());
    var_dump($e->getMessage());
}
```

Результатом виконання цього прикладу буде щось подібне:

```
string(16) "Custom_Exception"
string(6) "client"
```

### Дивіться також