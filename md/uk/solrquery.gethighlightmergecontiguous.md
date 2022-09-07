---
navigation:
  - solrquery.gethighlightmaxanalyzedchars.md: '« SolrQuery::getHighlightMaxAnalyzedChars'
  - solrquery.gethighlightregexmaxanalyzedchars.md: 'SolrQuery::getHighlightRegexMaxAnalyzedChars »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightMergeContiguous'
---
# SolrQuery::getHighlightMergeContiguous

(PECL solr> = 0.9.2)

SolrQuery::getHighlightMergeContiguous — Повертає, чи згорнути суміжні фрагменти в один фрагмент

### Опис

```methodsynopsis
public SolrQuery::getHighlightMergeContiguous(string $field_override = ?): bool
```

Повертає, чи повернути суміжні фрагменти в один фрагмент. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає логічне значення у разі успішного виконання та **`null`**, якщо значення не встановлено
