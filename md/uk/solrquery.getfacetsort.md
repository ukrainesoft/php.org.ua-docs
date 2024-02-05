---
navigation:
  - solrquery.getfacetqueries.md: '« SolrQuery::getFacetQueries'
  - solrquery.getfields.md: 'SolrQuery::getFields »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetSort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetSort

(PECL solr >= 0.9.2)

SolrQuery::getFacetSort — Повертає тип сортування фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetSort(string $field_override = ?): int
```

Повертає ціле число (SolrQuery::FACET\_SORT\_INDEX або SolrQuery::FACET\_SORT\_COUNT)

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число (SolrQuery::FACET\_SORT\_INDEX або SolrQuery::FACET\_SORT\_COUNT) у разі успішного виконання та **`null`**, якщо значення не встановлено
