---
navigation:
  - solrquery.gettermsupperbound.md: '« SolrQuery::getTermsUpperBound'
  - solrquery.removeexpandfilterquery.md: 'SolrQuery::removeExpandFilterQuery »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getTimeAllowed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getTimeAllowed

(PECL solr >= 0.9.2)

SolrQuery::getTimeAllowed — Повертає час у мілісекундах, дозволений для завершення запиту

### Опис

```methodsynopsis
public SolrQuery::getTimeAllowed(): int
```

Повертає час у мілісекундах, дозволений для завершення запиту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає і ціле число у разі успішного виконання та **`null`**, якщо визначений час не встановлено.
