---
navigation:
  - solrquery.getfacetmissing.html: '« SolrQuery::getFacetMissing'
  - solrquery.getfacetprefix.html: 'SolrQuery::getFacetPrefix »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::getFacetOffset'
---
# SolrQuery::getFacetOffset

(PECL solr> = 0.9.2)

SolrQuery::getFacetOffset — Повертає зсув у списку обмежень, які будуть використовуватися для посторінкової навігації

### Опис

```methodsynopsis
public SolrQuery::getFacetOffset(string $field_override = ?): int
```

Повертає усунення у списку обмежень, які будуть використовуватися для посторінкової навігації. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля, яке потрібно перевизначити.

### Значення, що повертаються

У разі успішного виконання повертає ціле число та **`null`**, якщо зміщення не встановлено
