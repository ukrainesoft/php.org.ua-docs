---
navigation:
  - solrquery.getfields.md: '« SolrQuery::getFields'
  - solrquery.getgroup.md: 'SolrQuery::getGroup »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFilterQueries'
---
# SolrQuery::getFilterQueries

(PECL solr> = 0.9.2)

SolrQuery::getFilterQueries — Повертає масив запитів фільтра

### Опис

```methodsynopsis
public SolrQuery::getFilterQueries(): array
```

Повертає масив запитів фільтру. Це запити, які можна використовувати для обмеження розширеного набору документів, які можна повернути, не впливаючи на оцінку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив у разі успішного виконання та **`null`**, якщо значення не встановлено
