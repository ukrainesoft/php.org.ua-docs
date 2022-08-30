Час, відведений на пошук

-   [« SolrQuery::setTermsUpperBound](solrquery.settermsupperbound.md)
    
-   [SolrDisMaxQuery »](class.solrdismaxquery.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Час, відведений на пошук
    

# SolrQuery::setTimeAllowed

(PECL solr> = 0.9.2)

SolrQuery::setTime Allowed — Час, відведений на пошук

### Опис

```methodsynopsis
public SolrQuery::setTimeAllowed(int $timeAllowed): SolrQuery
```

Час, відведений для завершення пошуку. Це значення стосується лише пошуку, а чи не запитів загалом. Час у мілісекундах. Значення, менші або рівні нулю, не передбачають обмеження часу. Часткові результати можуть бути повернуті, якщо вони є.

### Список параметрів

`timeAllowed`

Час, відведений для завершення пошуку.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.