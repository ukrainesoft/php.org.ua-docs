---
navigation:
  - yar-client.call.md: '« Yar\_Client::\_\_call'
  - yar-client.setopt.md: 'Yar\_Client::setOpt »'
  - index.md: PHP Manual
  - class.yar-client.md: Yar\_Client
title: 'Yar\_Client::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Client::\_\_construct

(PECL yar >= 1.0.0)

Yar\_Client::\_\_construct — Конструктор Yar\_Client

### Опис

```methodsynopsis
final public Yar_Client::__construct(string $url, array $options = ?)
```

Створює [Yar\_Client](class.yar-client.md)для[Yar\_Server](class.yar-server.md)

### Список параметрів

`url`

URL сервера Yar.

### Значення, що повертаються

Об'єкт класу [Yar\_Client](class.yar-client.md)

### Приклади

**Приклад #1 Приклад використання** Yar\_Client::\_\_construct()\*\*\*\*

```php
<?php
$client = new Yar_Client("http://host/api/");
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Client::\_\_call()](yar-client.call.md) \- Виклик сервісу
-   [Yar\_Client::setOpt()](yar-client.setopt.md) \- Задає контекст виклику
