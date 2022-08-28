Задає тип алгоритму, який слід використовувати під час фасетування поля

-   [« SolrQuery::setFacetLimit](solrquery.setfacetlimit.html)
    
-   [SolrQuery::setFacetMinCount »](solrquery.setfacetmincount.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Задає тип алгоритму, який слід використовувати під час фасетування поля
    

# SolrQuery::setFacetMethod

(PECL solr> = 0.9.2)

SolrQuery::setFacetMethod — Задає тип алгоритму, який слід використовувати під час фасетування поля

### Опис

```methodsynopsis
public SolrQuery::setFacetMethod(string $method, string $field_override = ?): SolrQuery
```

Задає тип алгоритму, який слід використовувати під час фасетування поля. Метод припускає перевизначення необов'язкового поля.

### Список параметрів

`method`

Використовуваний метод.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.