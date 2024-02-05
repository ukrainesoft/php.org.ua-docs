---
navigation:
  - solrquery.getfacetdatefields.md: '« SolrQuery::getFacetDateFields'
  - solrquery.getfacetdatehardend.md: 'SolrQuery::getFacetDateHardEnd »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetDateGap'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetDateGap

(PECL solr >= 0.9.2)

SolrQuery::getFacetDateGap — Повертає значення параметра facet.date.gap

### Опис

```methodsynopsis
public SolrQuery::getFacetDateGap(string $field_override = ?): string
```

Повертає значення facet.date.gap. Він приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
