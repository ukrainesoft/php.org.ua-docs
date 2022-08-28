Використовується для керування сортуванням результатів

-   [« SolrQuery::addMltQueryField](solrquery.addmltqueryfield.html)
    
-   [SolrQuery::addStatsFacet »](solrquery.addstatsfacet.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Використовується для керування сортуванням результатів
    

# SolrQuery::addSortField

(PECL solr> = 0.9.2)

SolrQuery::addSortField — Використовується для керування сортуванням результатів

### Опис

```methodsynopsis
public SolrQuery::addSortField(string $field, int $order = SolrQuery::ORDER_DESC): SolrQuery
```

Використовується для керування сортуванням результатів.

### Список параметрів

`field`

Назва поля

`order`

Напрямок сортування. Має бути або SolrQuery::ORDERASC, або SolrQuery::ORDERDESC.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery.