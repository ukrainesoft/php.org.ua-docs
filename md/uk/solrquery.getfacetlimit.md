Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету

-   [« SolrQuery::getFacetFields](solrquery.getfacetfields.md)
    
-   [SolrQuery::getFacetMethod »](solrquery.getfacetmethod.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету
    

# SolrQuery::getFacetLimit

(PECL solr> = 0.9.2)

SolrQuery::getFacetLimit — Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetLimit(string $field_override = ?): int
```

Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля, яке потрібно перевизначити

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено