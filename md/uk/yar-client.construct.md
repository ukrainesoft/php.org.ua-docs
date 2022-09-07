---
navigation:
  - yar-client.call.md: '« YarClient::call'
  - yar-client.setopt.md: 'YarClient::setOpt »'
  - index.md: PHP Manual
  - class.yar-client.md: YarClient
title: 'YarClient::construct'
---
# YarClient::construct

(PECL yar >= 1.0.0)

YarClient::construct — Конструктор YarClient

### Опис

```methodsynopsis
final public Yar_Client::__construct(string $url, array $options = ?)
```

Створює [YarClient](class.yar-client.md) для [YarServer](class.yar-server.md)

### Список параметрів

`url`

URL сервера Yar.

### Значення, що повертаються

Об'єкт класу [YarClient](class.yar-client.md)

### Приклади

**Приклад #1 Приклад використання **YarClient::construct()****

```php
<?php
$client = new Yar_Client("http://host/api/");
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarClient::call()](yar-client.call.md) - Виклик сервісу
-   [YarClient::setOpt()](yar-client.setopt.md) - Задати контекст виклику
