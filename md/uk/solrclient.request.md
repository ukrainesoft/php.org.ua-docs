---
navigation:
  - solrclient.query.md: '« SolrClient::query'
  - solrclient.rollback.md: 'SolrClient::rollback »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::request'
---
# SolrClient::request

(PECL solr> = 0.9.2)

SolrClient::request — Надсилає необроблений запит на оновлення

### Опис

```methodsynopsis
public SolrClient::request(string $raw_request): SolrUpdateResponse
```

Надсилає на сервер необроблений запит на оновлення XML

### Список параметрів

`raw_request`

Рядок XML з необробленим запитом до сервера.

### Значення, що повертаються

Повертає [SolrUpdateResponse](class.solrupdateresponse.md) у разі успішного виконання. Викидає виняток у разі помилки.

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md), якщо `raw_request` є порожнім рядком.

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrClient::request()****

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

$update_response = $client->request("<commit/>");

$response = $update_response->getResponse();

print_r($response);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
...
```
