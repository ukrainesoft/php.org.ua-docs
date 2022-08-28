Визначає запит фільтру

-   [« SolrQuery::addField](solrquery.addfield.html)
    
-   [SolrQuery::addGroupField »](solrquery.addgroupfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Визначає запит фільтру
    

# SolrQuery::addFilterQuery

(PECL solr> = 0.9.2)

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

**Приклад #1 Приклад використання **SolrQuery::addFilterQuery()****

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

$query = new SolrQuery();

$query->setQuery('*:*');

$query->addFilterQuery('color:blue,green');

$query_response = $client->query($query);

$response = $query_response->getResponse();

print_r($response['facet_counts']['facet_fields']);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
&fq=color:blue,green
```