---
navigation:
  - solrquery.settermsincludeupperbound.md: '« SolrQuery::setTermsIncludeUpperBound'
  - solrquery.settermslowerbound.md: 'SolrQuery::setTermsLowerBound »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setTermsLimit'
---
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
