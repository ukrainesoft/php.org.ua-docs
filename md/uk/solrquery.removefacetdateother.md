---
navigation:
  - solrquery.removefacetdatefield.md: '« SolrQuery::removeFacetDateField'
  - solrquery.removefacetfield.md: 'SolrQuery::removeFacetField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::removeFacetDateOther'
---
# SolrQuery::removeFacetDateOther

(PECL solr> = 0.9.2)

SolrQuery::removeFacetDateOther — Видалення одного з параметрів facet.date.other

### Опис

```methodsynopsis
public SolrQuery::removeFacetDateOther(string $value, string $field_override = ?): SolrQuery
```

Видаляє один із параметрів facet.date.other

### Список параметрів

`value`

Значення

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
