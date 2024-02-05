---
navigation:
  - solrquery.addexpandsortfield.md: '« SolrQuery::addExpandSortField'
  - solrquery.addfacetdateother.md: 'SolrQuery::addFacetDateOther »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addFacetDateField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addFacetDateField

(PECL solr >= 0.9.2)

SolrQuery::addFacetDateField — Карти для facet.date

### Опис

```methodsynopsis
public SolrQuery::addFacetDateField(string $dateField): SolrQuery
```

Метод дозволяє вказати поле, яке має розглядатись як фасет.

Може використовуватися кілька разів із різними іменами полів для вказівки кількох полів фасетів

### Список параметрів

`dateField`

Назва поля дати.

### Значення, що повертаються

Повертає об'єкт SolrQuery.
