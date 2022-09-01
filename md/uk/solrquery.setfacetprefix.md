---
navigation:
  - solrquery.setfacetoffset.html: '« SolrQuery::setFacetOffset'
  - solrquery.setfacetsort.html: 'SolrQuery::setFacetSort »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::setFacetPrefix'
---
# SolrQuery::setFacetPrefix

(PECL solr> = 0.9.2)

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
