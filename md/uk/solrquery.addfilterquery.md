---
navigation:
  - solrquery.addfield.md: '« SolrQuery::addField'
  - solrquery.addgroupfield.md: 'SolrQuery::addGroupField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addFilterQuery'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addFilterQuery

(PECL solr >= 0.9.2)

SolrQuery::addFilterQuery — Визначає запит фільтру

### Опис

```methodsynopsis
public SolrQuery::addFilterQuery(string $fq): SolrQuery
```

Визначає запит фільтру

### Список параметрів

`fq`

Фільтр запиту

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery.

### Приклади

**Пример #1 Пример использования**SolrQuery::addFilterQuery()\*\*\*\*

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

$query = new SolrQuery();

$query->setQuery('*:*');

$query->addFilterQuery('color:blue,green');

$query_response = $client->query($query);

$response = $query_response->getResponse();

print_r($response['facet_counts']['facet_fields']);

?>
```

Висновок наведеного прикладу буде схожим на:

```
&fq=color:blue,green
```
