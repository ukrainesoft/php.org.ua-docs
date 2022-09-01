---
navigation:
  - solrquery.setfacetmethod.html: '« SolrQuery::setFacetMethod'
  - solrquery.setfacetmissing.html: 'SolrQuery::setFacetMissing »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::setFacetMinCount'
---
# SolrQuery::setFacetMinCount

(PECL solr> = 0.9.2)

SolrQuery::setFacetMinCount — Відповідає facet.mincount

### Опис

```methodsynopsis
public SolrQuery::setFacetMinCount(int $mincount, string $field_override = ?): SolrQuery
```

Встановлює мінімальну кількість полів фасетів, які мають бути включені у відповідь

### Список параметрів

`mincount`

Мінімальна кількість

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
