---
navigation:
  - solrquery.getfacetmethod.md: '« SolrQuery::getFacetMethod'
  - solrquery.getfacetmissing.md: 'SolrQuery::getFacetMissing »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getFacetMinCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getFacetMinCount

(PECL solr >= 0.9.2)

SolrQuery::getFacetMinCount — Повертає мінімальну кількість полів аспектів, які повинні бути включені у відповідь

### Опис

```methodsynopsis
public SolrQuery::getFacetMinCount(string $field_override = ?): int
```

Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено
