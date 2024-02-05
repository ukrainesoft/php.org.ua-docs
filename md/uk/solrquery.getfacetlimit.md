---
navigation:
  - solrquery.getfacetfields.md: '« SolrQuery::getFacetFields'
  - solrquery.getfacetmethod.md: 'SolrQuery::getFacetMethod »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetLimit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetLimit

(PECL solr >= 0.9.2)

SolrQuery::getFacetLimit — Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetLimit(string $field_override = ?): int
```

Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля, яке потрібно перевизначити

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено
