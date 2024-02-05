---
navigation:
  - class.yar-client.md: « Yar\_Client
  - yar-client.construct.md: 'Yar\_Client::\_\_construct »'
  - index.md: PHP Manual
  - class.yar-client.md: Yar\_Client
title: 'Yar\_Client::\_\_call'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Client::\_\_call

(PECL yar >= 1.0.0)

Yar\_Client::\_\_call — Виклик сервісу

### Опис

```methodsynopsis
public Yar_Client::__call(string $method, array $parameters): void
```

Здійснює виклик віддаленого RPC-метода.

### Список параметрів

`method`

Ім'я дистанційного методу.

`parameters`

Параметри.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yar\_Client::\_\_call()\*\*\*\*

```php
<?php

$client = new Yar_Client("http://host/api/");

/* вызов удалённого сервиса */
$result = $client->some_method("parameter");
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Client::setOpt()](yar-client.setopt.md) \- Задає контекст виклику
