---
navigation:
  - solrquery.settermsupperbound.md: '« SolrQuery::setTermsUpperBound'
  - class.solrdismaxquery.md: SolrDisMaxQuery »
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setTimeAllowed'
---
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
