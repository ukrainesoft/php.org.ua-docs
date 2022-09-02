---
navigation:
  - solrquery.setfacetenumcachemindefaultfrequency.md: '« SolrQuery::setFacetEnumCacheMinDefaultFrequency'
  - solrquery.setfacetmethod.md: 'SolrQuery::setFacetMethod »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetLimit'
---
# SolrQuery::setFacetLimit

(PECL solr> = 0.9.2)

SolrQuery::setFacetLimit — Відповідає facet.limit

### Опис

```methodsynopsis
public SolrQuery::setFacetLimit(int $limit, string $field_override = ?): SolrQuery
```

Відповідає facet.limit. Встановлює максимальну кількість обмежень, які потрібно повернути для полів фасета.

### Список параметрів

`limit`

Максимальна кількість обмежень

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
