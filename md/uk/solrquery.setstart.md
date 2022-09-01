---
navigation:
  - solrquery.setshowdebuginfo.html: '« SolrQuery::setShowDebugInfo'
  - solrquery.setstats.html: 'SolrQuery::setStats »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::setStart'
---
# SolrQuery::setStart

(PECL solr> = 0.9.2)

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
