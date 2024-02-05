---
navigation:
  - solrquery.setshowdebuginfo.md: '« SolrQuery::setShowDebugInfo'
  - solrquery.setstats.md: 'SolrQuery::setStats »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setStart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setStart

(PECL solr >= 0.9.2)

SolrQuery::setStart — Визначає кількість рядків, що пропускаються.

### Опис

```methodsynopsis
public SolrQuery::setStart(int $start): SolrQuery
```

Визначає кількість рядків, що пропускаються. Корисно у розбивці на сторінки результатів.

### Список параметрів

`start`

Кількість пропущених рядків.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery.
