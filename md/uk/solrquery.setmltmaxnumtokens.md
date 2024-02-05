---
navigation:
  - solrquery.setmltmaxnumqueryterms.md: '« SolrQuery::setMltMaxNumQueryTerms'
  - solrquery.setmltmaxwordlength.md: 'SolrQuery::setMltMaxWordLength »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setMltMaxNumTokens'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setMltMaxNumTokens

(PECL solr >= 0.9.2)

SolrQuery::setMltMaxNumTokens — Задає максимальну кількість токенів для аналізу

### Опис

```methodsynopsis
public SolrQuery::setMltMaxNumTokens(int $value): SolrQuery
```

Задає максимальну кількість токенів для аналізу у кожному прикладі поля документа, яке не зберігається за допомогою TermVector.

### Список параметрів

`value`

Максимальна кількість токенів для аналізу

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
