- [« SolrQuery::addFacetField](solrquery.addfacetfield.md)
- [SolrQuery::addField »](solrquery.addfield.md)

- [PHP Manual](index.md)
- [SolrQuery](class.solrquery.md)
- Додає фасетний запит

# SolrQuery::addFacetQuery

(PECL solr \> = 0.9.2)

SolrQuery::addFacetQuery — Додає фасетний запит

### Опис

public **SolrQuery::addFacetQuery**(string `$facetQuery`):
[SolrQuery](class.solrquery.md)

Додає фасетний запит

### Список параметрів

`facetQuery`
Фасетний запит

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується повертається
значення.

### Приклади

**Приклад #1 Приклад використання
[SolrQuery::addFacetField()](solrquery.addfacetfield.md)**

` <?php$options = array(        'hostname' => SOLR_SERVER_HOSTNAME,        'login'    => SOLR_SERVER_USERNAME,        'password' => SOLR_SERVER_PASSWORD,        'port'     => SOLR_SERVER_PORT,);$client = new SolrClient($options);$ query = new SolrQuery('*:*');$query->setFacet(true);$query->addFacetQuery('price:[* TO 500]')->addFacetQuery('price:[500 TO *]') );$query_response = $client->query($query);$response = $query_response->getResponse();print_r($response->facet_counts->facet_queries);?> `

Результатом виконання цього прикладу буде щось подібне:


SolrObject Object
(
[price:[* TO 500]] => 14
[price:[500 TO *]] => 2
)
