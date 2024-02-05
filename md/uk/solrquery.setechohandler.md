---
navigation:
  - solrquery.removestatsfield.md: '« SolrQuery::removeStatsField'
  - solrquery.setechoparams.md: 'SolrQuery::setEchoParams »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setEchoHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setEchoHandler

(PECL solr >= 0.9.2)

SolrQuery::setEchoHandler — Перемикає параметр echoHandler

### Опис

```methodsynopsis
public SolrQuery::setEchoHandler(bool $flag): SolrQuery
```

Якщо встановлено значення true, Solr поміщає ім'я дескриптора, який використовується у відповіді, клієнту з метою налагодження.

### Список параметрів

`flag`

**`true`** або **`false`**

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
