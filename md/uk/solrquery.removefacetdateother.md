---
navigation:
  - solrquery.removefacetdatefield.html: '« SolrQuery::removeFacetDateField'
  - solrquery.removefacetfield.html: 'SolrQuery::removeFacetField »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
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
