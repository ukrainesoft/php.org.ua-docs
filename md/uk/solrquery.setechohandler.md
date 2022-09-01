---
navigation:
  - solrquery.removestatsfield.html: '« SolrQuery::removeStatsField'
  - solrquery.setechoparams.html: 'SolrQuery::setEchoParams »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::setEchoHandler'
---
# SolrQuery::setEchoHandler

(PECL solr> = 0.9.2)

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
