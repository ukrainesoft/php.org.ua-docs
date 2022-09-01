---
navigation:
  - solrquery.setfacetmissing.md: '« SolrQuery::setFacetMissing'
  - solrquery.setfacetprefix.md: 'SolrQuery::setFacetPrefix »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetOffset'
---
# SolrQuery::setFacetOffset

(PECL solr> = 0.9.2)

SolrQuery::setFacetOffset — Встановлює зміщення до списку обмежень для розбиття на сторінки

### Опис

```methodsynopsis
public SolrQuery::setFacetOffset(int $offset, string $field_override = ?): SolrQuery
```

Встановлює зміщення до списку обмежень розбивки на сторінки.

### Список параметрів

`offset`

Зміщення

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
