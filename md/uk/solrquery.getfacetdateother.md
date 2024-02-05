---
navigation:
  - solrquery.getfacetdatehardend.md: '« SolrQuery::getFacetDateHardEnd'
  - solrquery.getfacetdatestart.md: 'SolrQuery::getFacetDateStart »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetDateOther'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetDateOther

(PECL solr >= 0.9.2)

SolrQuery::getFacetDateOther — Повертає значення параметра facet.date.other

### Опис

```methodsynopsis
public SolrQuery::getFacetDateOther(string $field_override = ?): array
```

Повертає значення параметра facet.date.other. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає масив (array) у разі успішного виконання та **`null`**, якщо значення не встановлено
