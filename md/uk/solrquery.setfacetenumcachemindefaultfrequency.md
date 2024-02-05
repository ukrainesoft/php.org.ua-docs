---
navigation:
  - solrquery.setfacetdatestart.md: '« SolrQuery::setFacetDateStart'
  - solrquery.setfacetlimit.md: 'SolrQuery::setFacetLimit »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetEnumCacheMinDefaultFrequency'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setFacetEnumCacheMinDefaultFrequency

(PECL solr >= 0.9.2)

SolrQuery::setFacetEnumCacheMinDefaultFrequency — Встановлює мінімальну частоту документа, що використовується для визначення кількості виразів

### Опис

```methodsynopsis
public SolrQuery::setFacetEnumCacheMinDefaultFrequency(int $frequency, string $field_override = ?): SolrQuery
```

Встановлює мінімальну частоту документа, що використовується для визначення кількості виразів

### Список параметрів

`value`

Мінімальна частота

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
