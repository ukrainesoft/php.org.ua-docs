---
navigation:
  - solrquery.gethighlightregexpattern.md: '« SolrQuery::getHighlightRegexPattern'
  - solrquery.gethighlightrequirefieldmatch.md: 'SolrQuery::getHighlightRequireFieldMatch »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightRegexSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getHighlightRegexSlop

(PECL solr >= 0.9.2)

SolrQuery::getHighlightRegexSlop — Повертає коефіцієнт відхилення від ідеального розміру фрагмента

### Опис

```methodsynopsis
public SolrQuery::getHighlightRegexSlop(): float
```

Повертає коефіцієнт, який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента для відповідності регулярному виразу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає число з плаваючою точкою (float) у разі успішного виконання та **`null`**, якщо значення не встановлено.
