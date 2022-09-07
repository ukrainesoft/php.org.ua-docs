---
navigation:
  - class.yar-server.md: « YarServer
  - yar-server.handle.md: 'YarServer::handle »'
  - index.md: PHP Manual
  - class.yar-server.md: YarServer
title: 'YarServer::construct'
---
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

Об'єкт класу [YarServer](class.yar-server.md)

### Приклади

**Приклад #1 Приклад використання **YarServer::construct()****

```php
<?php
class API {
    /**
     * the doc info will be generated automatically into service info page.
     * @params
     * @return
     */
    public function some_method($parameter, $option = "foo") {
         return "some_method";
    }

    protected function client_can_not_see() {
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarServer::handle()](yar-server.handle.md) - Запустити сервер RPC
