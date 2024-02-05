---
navigation:
  - solrquery.getfacetdateother.md: '« SolrQuery::getFacetDateOther'
  - solrquery.getfacetfields.md: 'SolrQuery::getFacetFields »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetDateStart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetDateStart

(PECL solr >= 0.9.2)

SolrQuery::getFacetDateStart — Повертає нижню межу першого діапазону дат для всіх аспектів дати в цьому полі

### Опис

```methodsynopsis
public SolrQuery::getFacetDateStart(string $field_override = ?): string
```

Повертає нижню межу першого діапазону дат для всіх аспектів дати цього поля. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
