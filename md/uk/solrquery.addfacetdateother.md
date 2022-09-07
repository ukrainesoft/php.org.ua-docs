---
navigation:
  - solrquery.addfacetdatefield.md: '« SolrQuery::addFacetDateField'
  - solrquery.addfacetfield.md: 'SolrQuery::addFacetField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addFacetDateOther'
---
# SolrQuery::addFacetDateOther

(PECL solr> = 0.9.2)

SolrQuery::addFacetDateOther — Додає ще один параметр facet.date.other

### Опис

```methodsynopsis
public SolrQuery::addFacetDateOther(string $value, string $field_override = ?): SolrQuery
```

Встановлює параметр facet.date.other. Приймає необов'язкове перевизначення поля

### Список параметрів

`value`

Значення для використання.

`field_override`

Ім'я поля для перевизначення.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
