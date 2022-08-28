Визначає порядок обмежень поля фасету

-   [« SolrQuery::setFacetPrefix](solrquery.setfacetprefix.html)
    
-   [SolrQuery::setGroup »](solrquery.setgroup.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Визначає порядок обмежень поля фасету
    

# SolrQuery::setFacetSort

(PECL solr> = 0.9.2)

SolrQuery::setFacetSort — Визначає порядок обмежень поля фасету

### Опис

```methodsynopsis
public SolrQuery::setFacetSort(int $facetSort, string $field_override = ?): SolrQuery
```

Визначає порядок обмежень поля фасету

### Список параметрів

`facetSort`

Використовуйте SolrQuery::FACETSORTINDEX для сортування по порядку індексу або SolrQuery :: FACETSORTCOUNT для сортування за кількістю.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.