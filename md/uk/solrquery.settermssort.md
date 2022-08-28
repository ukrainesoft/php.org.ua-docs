Визначає, як сортувати повернені умови

-   [« SolrQuery::setTermsReturnRaw](solrquery.settermsreturnraw.html)
    
-   [SolrQuery::setTermsUpperBound »](solrquery.settermsupperbound.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Визначає, як сортувати повернені умови
    

# SolrQuery::setTermsSort

(PECL solr> = 0.9.2)

SolrQuery::setTermsSort — Визначає, як сортувати повернені умови.

### Опис

```methodsynopsis
public SolrQuery::setTermsSort(int $sortType): SolrQuery
```

Якщо SolrQuery::TERMSSORTCOUNT сортує терміни за частотою (найбільше спочатку). Якщо SolrQuery::TERMSSORTINDEX, повертає умови у порядку індексу

### Список параметрів

`sortType`

SolrQuery::TERMSSORTINDEX або SolrQuery::TERMSSORTCOUNT

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.