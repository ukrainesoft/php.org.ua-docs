---
navigation:
  - solrquery.setfacetoffset.md: '« SolrQuery::setFacetOffset'
  - solrquery.setfacetsort.md: 'SolrQuery::setFacetSort »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetPrefix'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setFacetPrefix

(PECL solr >= 0.9.2)

SolrQuery::setFacetPrefix — Визначає строковий префікс, за допомогою якого обмежуються вирази, на яких виконується фасет

### Опис

```methodsynopsis
public SolrQuery::setFacetPrefix(string $prefix, string $field_override = ?): SolrQuery
```

Визначає рядковий префікс, з якого обмежуються висловлювання, у яких виконується фасет.

### Список параметрів

`prefix`

Рядковий префікс

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
