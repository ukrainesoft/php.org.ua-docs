Встановлює максимальну кількість виразів, що повертаються.

-   [« SolrQuery::setTermsIncludeUpperBound](solrquery.settermsincludeupperbound.md)
    
-   [SolrQuery::setTermsLowerBound »](solrquery.settermslowerbound.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Встановлює максимальну кількість виразів, що повертаються.
    

# SolrQuery::setTermsLimit

(PECL solr> = 0.9.2)

SolrQuery::setTermsLimit — Встановлює максимальну кількість виразів, що повертаються.

### Опис

```methodsynopsis
public SolrQuery::setTermsLimit(int $limit): SolrQuery
```

Встановлює максимальну кількість виразів, що повертаються.

### Список параметрів

`limit`

Максимальна кількість термінів, що повертаються. Усі висловлювання буде повернено, якщо ліміт негативний.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.