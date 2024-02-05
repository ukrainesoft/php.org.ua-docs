---
navigation:
  - solrquery.addmltqueryfield.md: '« SolrQuery::addMltQueryField'
  - solrquery.addstatsfacet.md: 'SolrQuery::addStatsFacet »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addSortField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addSortField

(PECL solr >= 0.9.2)

SolrQuery::addSortField — Використовується для керування сортуванням результатів

### Опис

```methodsynopsis
public SolrQuery::addSortField(string $field, int $order = SolrQuery::ORDER_DESC): SolrQuery
```

Використовується для керування сортуванням результатів.

### Список параметрів

`field`

Назва поля

`order`

Напрямок сортування. Має бути або SolrQuery::ORDER\_ASC, або SolrQuery::ORDER\_DESC.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery.
