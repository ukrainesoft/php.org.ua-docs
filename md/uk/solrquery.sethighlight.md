---
navigation:
  - solrquery.setgrouptruncate.md: '« SolrQuery::setGroupTruncate'
  - solrquery.sethighlightalternatefield.md: 'SolrQuery::setHighlightAlternateField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlight'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlight

(PECL solr >= 0.9.2)

SolrQuery::setHighlight — Вмикає або вимикає виділення

### Опис

```methodsynopsis
public SolrQuery::setHighlight(bool $flag): SolrQuery
```

Установив значение\*\*`true`\*\* дозволяє створювати виділені фрагменти у відповіді запит.

Установив значение\*\*`false`\*\* відключає виділення

### Список параметрів

`flag`

Вмикає або вимикає виділення

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
