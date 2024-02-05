---
navigation:
  - solrquery.setstart.md: '« SolrQuery::setStart'
  - solrquery.setterms.md: 'SolrQuery::setTerms »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setStats'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setStats

(PECL solr >= 0.9.2)

SolrQuery::setStats — Вмикає або вимикає компонент Stats

### Опис

```methodsynopsis
public SolrQuery::setStats(bool $flag): SolrQuery
```

Вмикає або вимикає компонент Stats.

### Список параметрів

`flag`

**`true`** включає компонент Stats, а **`false`** відключає.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
