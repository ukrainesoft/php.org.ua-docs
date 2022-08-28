Повертає тип сортування фасету

-   [« SolrQuery::getFacetQueries](solrquery.getfacetqueries.html)
    
-   [SolrQuery::getFields »](solrquery.getfields.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає тип сортування фасету
    

# SolrQuery::getFacetSort

(PECL solr> = 0.9.2)

SolrQuery::getFacetSort — Повертає тип сортування фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetSort(string $field_override = ?): int
```

Повертає ціле число (SolrQuery::FACETSORTINDEX або SolrQuery::FACETSORTCOUNT)

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число (SolrQuery::FACETSORTINDEX або SolrQuery::FACETSORTCOUNT) у разі успішного виконання та **`null`**, якщо значення не встановлено