---
navigation:
  - solrquery.setgrouptruncate.md: '« SolrQuery::setGroupTruncate'
  - solrquery.sethighlightalternatefield.md: 'SolrQuery::setHighlightAlternateField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlight'
---
# SolrQuery::setHighlight

(PECL solr> = 0.9.2)

SolrQuery::setHighlight — Вмикає або вимикає виділення

### Опис

```methodsynopsis
public SolrQuery::setHighlight(bool $flag): SolrQuery
```

Встановивши значення **`true`** дозволяє створювати виділені фрагменти у відповіді запит.

Встановивши значення **`false`** відключає виділення

### Список параметрів

`flag`

Вмикає або вимикає виділення

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
