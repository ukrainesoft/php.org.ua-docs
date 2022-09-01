---
navigation:
  - solrquery.getfacet.html: '« SolrQuery::getFacet'
  - solrquery.getfacetdatefields.html: 'SolrQuery::getFacetDateFields »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::getFacetDateEnd'
---
# SolrQuery::getFacetDateEnd

(PECL solr> = 0.9.2)

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
