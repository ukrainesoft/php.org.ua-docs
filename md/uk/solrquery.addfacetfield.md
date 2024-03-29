---
navigation:
  - solrquery.addfacetdateother.md: '« SolrQuery::addFacetDateOther'
  - solrquery.addfacetquery.md: 'SolrQuery::addFacetQuery »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addFacetField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addFacetField

(PECL solr >= 0.9.2)

SolrQuery::addFacetField — Додає інше поле до фасету

### Опис

```methodsynopsis
public SolrQuery::addFacetField(string $field): SolrQuery
```

Додає інше поле до фасету

### Список параметрів

`field`

Назва поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.

### Приклади

**Приклад #1 Приклад використання** SolrQuery::addFacetField()\*\*\*\*

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

$query->setQuery($query);

$query->addField('price')->addField('color');

$query->setFacet(true);

$query->addFacetField('price')->addFacetField('color');

$query_response = $client->query($query);

$response = $query_response->getResponse();

print_r($response['facet_counts']['facet_fields']);

?>
```

Висновок наведеного прикладу буде схожим на:

```
SolrObject Object
(
    [color] => SolrObject Object
        (
            [blue] => 20
            [green] => 100
        )

)
```
