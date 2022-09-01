---
navigation:
  - mysql-xdevapi-client.close.html: '« mysqlxdevapiClient::close'
  - mysql-xdevapi-client.getsession.html: 'Client::getClient »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-client.html: mysqlxdevapiClient
title: 'Client::construct'
---
# Client::construct

(No version information available, might only be in Git)

Client::construct - Конструктор класу Client

### Опис

private **mysqlxdevapiClient::construct**

Конструктор класу Client.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiClient::construct()****

```php
<?php
$pooling_options = '{
  "enabled": true,
    "maxSize": 10,
    "maxIdleTime": 3600,
    "queueTimeOut": 1000
}';
$client = mysql_xdevapi\getClient($connection_uri, $pooling_options);
$session = $client->getSession();
```
