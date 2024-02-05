---
navigation:
  - solrquery.getfacetmincount.md: '« SolrQuery::getFacetMinCount'
  - solrquery.getfacetoffset.md: 'SolrQuery::getFacetOffset »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetMissing'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetMissing

(PECL solr >= 0.9.2)

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
