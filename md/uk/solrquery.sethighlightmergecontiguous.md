---
navigation:
  - solrquery.sethighlightmaxanalyzedchars.md: '« SolrQuery::setHighlightMaxAnalyzedChars'
  - solrquery.sethighlightregexmaxanalyzedchars.md: 'SolrQuery::setHighlightRegexMaxAnalyzedChars »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightMergeContiguous'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightMergeContiguous

(PECL solr >= 0.9.2)

SolrQuery::setHighlightMergeContiguous — Чи згортати суміжні фрагменти в один фрагмент

### Опис

```methodsynopsis
public SolrQuery::setHighlightMergeContiguous(bool $flag, string $field_override = ?): SolrQuery
```

Чи згортати суміжні фрагменти в один фрагмент

### Список параметрів

`value`

Чи згортати суміжні фрагменти в один фрагмент

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
