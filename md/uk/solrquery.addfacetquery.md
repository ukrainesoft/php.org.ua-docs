---
navigation:
  - solrquery.addfacetfield.md: '« SolrQuery::addFacetField'
  - solrquery.addfield.md: 'SolrQuery::addField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addFacetQuery'
---
# SolrQuery::addFacetQuery

(PECL solr> = 0.9.2)

SolrQuery::addFacetQuery — Додає фасетний запит

### Опис

```methodsynopsis
public SolrQuery::addFacetQuery(string $facetQuery): SolrQuery
```

Додає фасетний запит

### Список параметрів

`facetQuery`

Фасетний запит

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.

### Приклади

**Приклад #1 Приклад використання [SolrQuery::addFacetField()](solrquery.addfacetfield.md)**

```php
<?php

$options = array
(
        'hostname' => SOLR_SERVER_HOSTNAME,
        'login'    => SOLR_SERVER_USERNAME,
        'password' => SOLR_SERVER_PASSWORD,
        'port'     => SOLR_SERVER_PORT,
);

$client = new SolrClient($options);

$query = new SolrQuery('*:*');

$query->setFacet(true);

$query->addFacetQuery('price:[* TO 500]')->addFacetQuery('price:[500 TO *]');

$query_response = $client->query($query);

$response = $query_response->getResponse();

print_r($response->facet_counts->facet_queries);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
SolrObject Object
(
    [price:[* TO 500]] => 14
    [price:[500 TO *]] => 2
)
```
