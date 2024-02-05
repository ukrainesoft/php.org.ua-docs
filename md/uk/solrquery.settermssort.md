---
navigation:
  - solrquery.settermsreturnraw.md: '« SolrQuery::setTermsReturnRaw'
  - solrquery.settermsupperbound.md: 'SolrQuery::setTermsUpperBound »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setTermsSort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setTermsSort

(PECL solr >= 0.9.2)

SolrQuery::setTermsSort — Визначає, як сортувати повернені умови.

### Опис

```methodsynopsis
public SolrQuery::setTermsSort(int $sortType): SolrQuery
```

Якщо SolrQuery::TERMS\_SORT\_COUNT сортує терміни за частотою (найбільше спочатку). Якщо SolrQuery::TERMS\_SORT\_INDEX, повертає умови у порядку індексу

### Список параметрів

`sortType`

SolrQuery::TERMS\_SORT\_INDEX або SolrQuery::TERMS\_SORT\_COUNT

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
