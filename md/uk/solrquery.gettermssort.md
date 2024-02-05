---
navigation:
  - solrquery.gettermsreturnraw.md: '« SolrQuery::getTermsReturnRaw'
  - solrquery.gettermsupperbound.md: 'SolrQuery::getTermsUpperBound »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getTermsSort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getTermsSort

(PECL solr >= 0.9.2)

SolrQuery::getTermsSort — Повертає ціле число, що вказує, як сортуються вирази

### Опис

```methodsynopsis
public SolrQuery::getTermsSort(): int
```

SolrQuery::TERMS\_SORT\_INDEX вказує, що вирази повертаються у порядку індексу. SolrQuery::TERMS\_SORT\_COUNT має на увазі, що вирази сортуються за частотою виразу (спочатку найвищу кількість)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає ціле число та **`null`**, якщо значення не встановлено.
