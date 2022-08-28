Повертає стан параметра facet.missing

-   [« SolrQuery::getFacetMinCount](solrquery.getfacetmincount.html)
    
-   [SolrQuery::getFacetOffset »](solrquery.getfacetoffset.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає стан параметра facet.missing
    

# SolrQuery::getFacetMissing

(PECL solr> = 0.9.2)

SolrQuery::getFacetMissing — Повертає поточний стан facet.missing

### Опис

```methodsynopsis
public SolrQuery::getFacetMissing(string $field_override = ?): bool
```

Повертає поточний стан facet.missing. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає логічне значення у разі успішного виконання та **`null`**, якщо значення не встановлено