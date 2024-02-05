---
navigation:
  - solrquery.sethighlightregexpattern.md: '« SolrQuery::setHighlightRegexPattern'
  - solrquery.sethighlightrequirefieldmatch.md: 'SolrQuery::setHighlightRequireFieldMatch »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightRegexSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightRegexSlop

(PECL solr >= 0.9.2)

SolrQuery::setHighlightRegexSlop — Встановлює коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента

### Опис

```methodsynopsis
public SolrQuery::setHighlightRegexSlop(float $factor): SolrQuery
```

Коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента (зазначеного SolrQuery::setHighlightFragsize) для відповідності регулярному виразу.

### Список параметрів

`factor`

Коефіцієнт, який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
