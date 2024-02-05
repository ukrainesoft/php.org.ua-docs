---
navigation:
  - solrquery.getmltmaxwordlength.md: '« SolrQuery::getMltMaxWordLength'
  - solrquery.getmltmintermfrequency.md: 'SolrQuery::getMltMinTermFrequency »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getMltMinDocFrequency'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getMltMinDocFrequency

(PECL solr >= 0.9.2)

SolrQuery::getMltMinDocFrequency — Повертає граничну частоту, з якої будуть ігноруватися слова, яких немає, принаймні, у такій кількості документів

### Опис

```methodsynopsis
public SolrQuery::getMltMinDocFrequency(): int
```

Повертає граничну частоту, з якої ігноруватимуться слова, яких немає, принаймні, у такій кількості документів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає ціле число та **`null`**, якщо значення не встановлено.
