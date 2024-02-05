---
navigation:
  - solrquery.sethighlightmergecontiguous.md: '« SolrQuery::setHighlightMergeContiguous'
  - solrquery.sethighlightregexpattern.md: 'SolrQuery::setHighlightRegexPattern »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightRegexMaxAnalyzedChars'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightRegexMaxAnalyzedChars

(PECL solr >= 0.9.2)

SolrQuery::setHighlightRegexMaxAnalyzedChars — Задає максимальну кількість символів для аналізу

### Опис

```methodsynopsis
public SolrQuery::setHighlightRegexMaxAnalyzedChars(int $maxAnalyzedChars): SolrQuery
```

Задає максимальну кількість символів для аналізу з поля під час використання фрагментера регулярного виразу

### Список параметрів

`maxAnalyzedChars`

Максимальна кількість символів для аналізу з поля під час використання фрагментера регулярного виразу

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
