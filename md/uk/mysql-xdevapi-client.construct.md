---
navigation:
  - mysql-xdevapi-client.close.md: '« mysql\_xdevapi\\Client::close'
  - mysql-xdevapi-client.getsession.md: 'Client::getClient »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-client.md: mysql\_xdevapi\\Client
title: 'Client::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Client::\_\_construct

(No version information available, might only be in Git)

Client::\_\_construct — Конструктор класу Client

### Опис

private**mysql\_xdevapi\\Client::\_\_construct**()

Конструктор класу Client.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Client::\_\_construct()\*\*\*\*

```php
<?php
$pooling_options = '{
  "enabled": true,
    "maxSize": 10,
    "maxIdleTime": 3600,
    "queueTimeOut": 1000
}';
$client = mysql_xdevapi\getClient($connection_uri, $pooling_options);
$session = $client->getSession();
```
