---
navigation:
  - solrquery.getfacetoffset.md: '« SolrQuery::getFacetOffset'
  - solrquery.getfacetqueries.md: 'SolrQuery::getFacetQueries »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetPrefix'
---
# SolrQuery::getFacetPrefix

(PECL solr> = 0.9.2)

SolrQuery::getFacetPrefix — Повертає префікс фасету

### Опис

```methodsynopsis
public SolrQuery::getFacetPrefix(string $field_override = ?): string
```

Повертає префікс фасету

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
