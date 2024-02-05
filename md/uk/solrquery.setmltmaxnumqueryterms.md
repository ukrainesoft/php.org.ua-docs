---
navigation:
  - solrquery.setmltcount.md: '« SolrQuery::setMltCount'
  - solrquery.setmltmaxnumtokens.md: 'SolrQuery::setMltMaxNumTokens »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setMltMaxNumQueryTerms'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setMltMaxNumQueryTerms

(PECL solr >= 0.9.2)

SolrQuery::setMltMaxNumQueryTerms — Встановлює максимальну кількість запитів, що включаються.

### Опис

```methodsynopsis
public SolrQuery::setMltMaxNumQueryTerms(int $value): SolrQuery
```

Встановлює максимальну кількість виразів запиту, які будуть включені до будь-якого згенерованого запиту.

### Список параметрів

`value`

Максимальна кількість виразів запиту, які будуть включені до будь-якого згенерованого запиту

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
