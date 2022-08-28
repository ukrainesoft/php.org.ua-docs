Повертає значення параметра facet.method

-   [« SolrQuery::getFacetLimit](solrquery.getfacetlimit.html)
    
-   [SolrQuery::getFacetMinCount »](solrquery.getfacetmincount.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
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