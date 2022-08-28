Конструктор YarServer

-   [« Yar\_Server](class.yar-server.html)
    
-   [Yar\_Server::handle »](yar-server.handle.html)
    
-   [PHP Manual](index.html)
    
-   [Yar\_Server](class.yar-server.html)
    
-   Конструктор YarServer
    

# YarServer::construct

(PECL yar >= 1.0.0)

YarServer::construct — Конструктор YarServer

### Опис

```methodsynopsis
final public Yar_Server::__construct(Object $obj)
```

Встановлює сервер Yar HTTP RPC. Усі публічні методи об'єкта $obj будуть зареєстровані як RPC-сервіси.

### Список параметрів

`obj`

Об'єкт, публічні методи якого буде зареєстровано як RPC-сервисы.

### Значення, що повертаються

Об'єкт класу [Yar\_Server](class.yar-server.html)

### Приклади

**Приклад #1 Приклад використання **YarServer::construct()****

```php
<?php
class API {
    /**
     * the doc info will be generated automatically into service info page.
     * @params
     * @return
     */
    public function some_method($parameter, $option = "foo") {
         return "some_method";
    }

    protected function client_can_not_see() {
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [Yar\_Server::handle()](yar-server.handle.html) - Запустити сервер RPC