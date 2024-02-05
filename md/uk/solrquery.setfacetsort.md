---
navigation:
  - solrquery.setfacetprefix.md: '« SolrQuery::setFacetPrefix'
  - solrquery.setgroup.md: 'SolrQuery::setGroup »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetSort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setFacetSort

(PECL solr >= 0.9.2)

SolrQuery::setFacetSort — Визначає порядок обмежень поля фасету

### Опис

```methodsynopsis
public SolrQuery::setFacetSort(int $facetSort, string $field_override = ?): SolrQuery
```

Визначає порядок обмежень поля фасету

### Список параметрів

`facetSort`

Використовуйте SolrQuery::FACET\_SORT\_INDEX для сортування по порядку індексу або SolrQuery :: FACET\_SORT\_COUNT для сортування за кількістю.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
