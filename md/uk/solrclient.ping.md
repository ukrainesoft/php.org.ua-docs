---
navigation:
  - solrclient.optimize.md: '« SolrClient::optimize'
  - solrclient.query.md: 'SolrClient::query »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::ping'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::ping

(PECL solr >= 0.9.2)

SolrClient::ping — Перевіряє, чи працює сервер Solr

### Опис

```methodsynopsis
public SolrClient::ping(): SolrPingResponse
```

Перевіряє, чи доступний сервер Solr. Надсилає запит HEAD на сервер Apache Solr.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SolrPingResponse](class.solrpingresponse.md) у разі успішного виконання або викидає виняток у разі виникнення помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Приклади

**Пример #1 Пример использования**SolrClient::ping()\*\*\*\*

```php
<?php
$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
);

$client = new SolrClient($options);

$pingresponse = $client->ping();

?>
```

Висновок наведеного прикладу буде схожим на:
