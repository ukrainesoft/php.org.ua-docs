---
navigation:
  - class.yar-server.md: « Yar\_Server
  - yar-server.handle.md: 'Yar\_Server::handle »'
  - index.md: PHP Manual
  - class.yar-server.md: Yar\_Server
title: 'Yar\_Server::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Server::\_\_construct

(PECL yar >= 1.0.0)

Yar\_Server::\_\_construct — Конструктор Yar\_Server

### Опис

```methodsynopsis
final public Yar_Server::__construct(Object $obj)
```

Встановлює сервер Yar HTTP RPC. Усі публічні методи об'єкта $obj будуть зареєстровані як RPC-сервіси.

### Список параметрів

`obj`

Об'єкт, публічні методи якого буде зареєстровано як RPC-сервисы.

### Значення, що повертаються

Об'єкт класу [Yar\_Server](class.yar-server.md)

### Приклади

**Пример #1 Пример использования**Yar\_Server::\_\_construct()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Server::handle()](yar-server.handle.md) \- Запустити сервер RPC
