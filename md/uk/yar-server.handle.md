---
navigation:
  - yar-server.construct.md: '« Yar\_Server::\_\_construct'
  - class.yar-client.md: Yar\_Client »
  - index.md: PHP Manual
  - class.yar-server.md: Yar\_Server
title: 'Yar\_Server::handle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Server::handle

(PECL yar >= 1.0.0)

Yar\_Server::handle — Запустити сервер RPC

### Опис

```methodsynopsis
public Yar_Server::handle(): bool
```

Запустити сервер RPC HTTP і підготуватися приймати запити.

> **Зауваження** :
> 
> Зазвичай RPC-запити здійснюються за допомогою HTTP POST. Якщо буде використано запит HTTP GET, то буде надруковано інформацію про сервіс (закоментована секція вище).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

boolean

### Приклади

**Приклад #1 Приклад використання** Yar\_Server::handle()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Server::\_\_construct()](yar-server.construct.md) \- Конструктор Yar\_Server
