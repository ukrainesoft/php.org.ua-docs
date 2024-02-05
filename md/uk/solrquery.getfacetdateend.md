---
navigation:
  - solrquery.getfacet.md: '« SolrQuery::getFacet'
  - solrquery.getfacetdatefields.md: 'SolrQuery::getFacetDateFields »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetDateEnd'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetDateEnd

(PECL solr >= 0.9.2)

SolrQuery::getFacetDateEnd — Повертає значення параметра facet.date.end

### Опис

```methodsynopsis
public SolrQuery::getFacetDateEnd(string $field_override = ?): string
```

Повертає значення facet.date.end. Метод приймає необов'язкове перевизначення поля.

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
