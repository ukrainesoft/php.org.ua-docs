Вказує, які поля повертати в результаті

-   [« SolrQuery::addFacetQuery](solrquery.addfacetquery.html)
    
-   [SolrQuery::addFilterQuery »](solrquery.addfilterquery.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Вказує, які поля повертати в результаті
    

# SolrQuery::addField

(PECL solr> = 0.9.2)

SolrQuery::addField — Вказує, які поля повертати в результаті

### Опис

```methodsynopsis
public SolrQuery::addField(string $field): SolrQuery
```

Метод використовується для вказівки набору полів для повернення, тим самим обмежуючи обсяг даних, що повертаються у відповіді.

Він повинен викликатись кілька разів, по одному разу для кожного імені поля.

### Список параметрів

`field`

Назва поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery