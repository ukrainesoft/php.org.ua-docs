---
navigation:
  - solrquery.setmltcount.md: '« SolrQuery::setMltCount'
  - solrquery.setmltmaxnumtokens.md: 'SolrQuery::setMltMaxNumTokens »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setMltMaxNumQueryTerms'
---
# SolrQuery::setMltMaxNumQueryTerms

(PECL solr> = 0.9.2)

SolrQuery::setMltMaxNumQueryTerms — Встановлює максимальну кількість запитів, що включаються.

### Опис

```methodsynopsis
public SolrQuery::setMltMaxNumQueryTerms(int $value): SolrQuery
```

Встановлює максимальну кількість запитів, які будуть включені в будь-який згенерований запит.

### Список параметрів

`value`

Максимальна кількість виразів запиту, які будуть включені до будь-якого згенерованого запиту

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
