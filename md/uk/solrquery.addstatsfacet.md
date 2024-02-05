---
navigation:
  - solrquery.addsortfield.md: '« SolrQuery::addSortField'
  - solrquery.addstatsfield.md: 'SolrQuery::addStatsField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addStatsFacet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addStatsFacet

(PECL solr >= 0.9.2)

SolrQuery::addStatsFacet — Вимагає повернення допоміжних результатів для значень у цьому фасеті

### Опис

```methodsynopsis
public SolrQuery::addStatsFacet(string $field): SolrQuery
```

Запитує повернення допоміжних результатів для значень у фасеті. Відповідає полю stats.facet

### Список параметрів

`field`

Назва поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
