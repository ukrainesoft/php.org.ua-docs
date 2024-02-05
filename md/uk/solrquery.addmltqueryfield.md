---
navigation:
  - solrquery.addmltfield.md: '« SolrQuery::addMltField'
  - solrquery.addsortfield.md: 'SolrQuery::addSortField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addMltQueryField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addMltQueryField

(PECL solr >= 0.9.2)

SolrQuery::addMltQueryField — Відповідає mlt.qf

### Опис

```methodsynopsis
public SolrQuery::addMltQueryField(string $field, float $boost): SolrQuery
```

Відповідає mlt.qf. Використовується для вказівки полів запиту та їх підвищення.

### Список параметрів

`field`

Назва поля

`boost`

Значення підвищення

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
