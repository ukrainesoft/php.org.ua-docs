Повертає значення параметра facet.method

-   [« SolrQuery::getFacetLimit](solrquery.getfacetlimit.md)
    
-   [SolrQuery::getFacetMinCount »](solrquery.getfacetmincount.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Повертає значення параметра facet.method
    

# SolrQuery::getFacetMethod

(PECL solr> = 0.9.2)

SolrQuery::getFacetMethod — Повертає значення параметра facet.method

### Опис

```methodsynopsis
public SolrQuery::getFacetMethod(string $field_override = ?): string
```

Повертає значення параметра facet.method. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено