---
navigation:
  - yar-server.construct.md: '« YarServer::construct'
  - class.yar-client.md: YarClient »
  - index.md: PHP Manual
  - class.yar-server.md: YarServer
title: 'YarServer::handle'
---
# YarServer::handle

(PECL yar >= 1.0.0)

YarServer::handle — Запустити сервер RPC

### Опис

```methodsynopsis
public Yar_Server::handle(): bool
```

Запустити сервер RPC HTTP і підготуватися приймати запити.

> **Зауваження**
> 
> Зазвичай RPC-запити здійснюються за допомогою HTTP POST. Якщо буде використано запит HTTP GET, то буде надруковано інформацію про сервіс (закоментована секція вище).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

boolean

### Приклади

**Приклад #1 Приклад використання **YarServer::handle()****

```php
<?php
class API {
    /**
     * the doc info will be generated automatically into service info page.
     * @params
     * @return
     */
    public function some_method($parameter, $option = "foo") {
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

-   [YarServer::construct()](yar-server.construct.md) - Конструктор YarServer
