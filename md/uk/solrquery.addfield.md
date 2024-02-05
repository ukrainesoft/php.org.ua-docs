---
navigation:
  - solrquery.addfacetquery.md: '« SolrQuery::addFacetQuery'
  - solrquery.addfilterquery.md: 'SolrQuery::addFilterQuery »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addField

(PECL solr >= 0.9.2)

SolrQuery::addField — Вказує, які поля повертати в результаті

### Опис

```methodsynopsis
public SolrQuery::addField(string $field): SolrQuery
```

Метод використовується для вказівки набору полів для повернення, тим самим обмежуючи обсяг даних, що повертаються у відповіді.

Він має викликатись кілька разів, по одному разу для кожного імені поля.

### Список параметрів

`field`

Назва поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery
