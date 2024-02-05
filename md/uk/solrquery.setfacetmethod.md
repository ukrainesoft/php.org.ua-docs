---
navigation:
  - solrquery.setfacetlimit.md: '« SolrQuery::setFacetLimit'
  - solrquery.setfacetmincount.md: 'SolrQuery::setFacetMinCount »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetMethod'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setFacetMethod

(PECL solr >= 0.9.2)

SolrQuery::setFacetMethod — Задає тип алгоритму, який слід використовувати під час фасетування поля

### Опис

```methodsynopsis
public SolrQuery::setFacetMethod(string $method, string $field_override = ?): SolrQuery
```

Задає тип алгоритму, який слід використовувати під час фасетування поля. Метод припускає перевизначення необов'язкового поля.

### Список параметрів

`method`

Використовуваний метод.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
