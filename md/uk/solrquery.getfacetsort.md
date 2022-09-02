---
navigation:
  - solrquery.getfacetqueries.md: '« SolrQuery::getFacetQueries'
  - solrquery.getfields.md: 'SolrQuery::getFields »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetSort'
---
# SolrQuery::getFacetSort

(PECL solr> = 0.9.2)

SolrQuery::getFacetSort — Повертає тип сортування фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetSort(string $field_override = ?): int
```

Повертає ціле число (SolrQuery::FACETSORTINDEX або SolrQuery::FACETSORTCOUNT)

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число (SolrQuery::FACETSORTINDEX або SolrQuery::FACETSORTCOUNT) у разі успішного виконання та **`null`**, якщо значення не встановлено
