---
navigation:
  - class.solrcollapsefunction.md: « SolrCollapseFunction
  - solrcollapsefunction.getfield.md: 'SolrCollapseFunction::getField »'
  - index.md: PHP Manual
  - class.solrcollapsefunction.md: SolrCollapseFunction
title: 'SolrCollapseFunction::construct'
---
# SolrCollapseFunction::construct

(PECL solr> = 2.2.0)

SolrCollapseFunction::construct - Конструктор класу

### Опис

public **SolrCollapseFunction::construct**(string `$field`

Конструктор класу Collapse Function

### Список параметрів

`field`

Ім'я поля для згортання.

Щоб згорнути результат. Тип поля має бути однозначним: рядок, ціле число чи число з плаваючою точкою.

### Приклади

**Приклад #1 Приклад використання **SolrCollapseFunction::construct()****

```php
<?php

include "bootstrap.php";

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
    'path'     => SOLR_SERVER_PATH
);

$client = new SolrClient($options);

$query = new SolrQuery('*:*');

$func = new SolrCollapseFunction('field_name');

$func->setMax('sum(cscore(),field(some_other_field))');
$func->setSize(100);
$func->setNullPolicy(SolrCollapseFunction::NULLPOLICY_EXPAND);

$query->collapse($func);

$queryResponse = $client->query($query);

$response = $queryResponse->getResponse();

print_r($response);

?>
```

### Дивіться також

-   [SolrQuery::collapse()](solrquery.collapse.md) - Згортає набір результатів до одного документа на групу
