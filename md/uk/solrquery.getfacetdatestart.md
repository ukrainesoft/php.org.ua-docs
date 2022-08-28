Повертає нижню межу першого діапазону дат для всіх аспектів дати у цьому полі

-   [« SolrQuery::getFacetDateOther](solrquery.getfacetdateother.html)
    
-   [SolrQuery::getFacetFields »](solrquery.getfacetfields.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає нижню межу першого діапазону дат для всіх аспектів дати у цьому полі
    

# SolrQuery::getFacetDateStart

(PECL solr> = 0.9.2)

SolrQuery::getFacetDateStart — Повертає нижню межу першого діапазону дат для всіх аспектів дати в цьому полі

### Опис

```methodsynopsis
public SolrQuery::getFacetDateStart(string $field_override = ?): string
```

Повертає нижню межу першого діапазону дат для всіх аспектів дати цього поля. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено