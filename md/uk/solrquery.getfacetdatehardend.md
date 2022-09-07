---
navigation:
  - solrquery.getfacetdategap.md: '« SolrQuery::getFacetDateGap'
  - solrquery.getfacetdateother.md: 'SolrQuery::getFacetDateOther »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetDateHardEnd'
---
# SolrQuery::getFacetDateHardEnd

(PECL solr> = 0.9.2)

SolrQuery::getFacetDateHardEnd — Повертає значення параметра facet.date.hardend

### Опис

```methodsynopsis
public SolrQuery::getFacetDateHardEnd(string $field_override = ?): string
```

Повертає значення параметра facet.date.hardend. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
