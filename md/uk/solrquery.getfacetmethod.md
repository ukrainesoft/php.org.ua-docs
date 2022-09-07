---
navigation:
  - solrquery.getfacetlimit.md: '« SolrQuery::getFacetLimit'
  - solrquery.getfacetmincount.md: 'SolrQuery::getFacetMinCount »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetMethod'
---
# SolrQuery::getFacetMethod

(PECL solr> = 0.9.2)

SolrQuery::getFacetMethod — Повертає значення параметра facet.method

### Опис

```methodsynopsis
public SolrQuery::getFacetMethod(string $field_override = ?): string
```

Повертає значення параметра facet.method. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
