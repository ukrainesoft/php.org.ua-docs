---
navigation:
  - solrquery.getfacetmincount.html: '« SolrQuery::getFacetMinCount'
  - solrquery.getfacetoffset.html: 'SolrQuery::getFacetOffset »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::getFacetMissing'
---
# SolrQuery::getFacetMissing

(PECL solr> = 0.9.2)

SolrQuery::getFacetMissing — Повертає поточний стан facet.missing

### Опис

```methodsynopsis
public SolrQuery::getFacetMissing(string $field_override = ?): bool
```

Повертає поточний стан facet.missing. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає логічне значення у разі успішного виконання та **`null`**, якщо значення не встановлено
