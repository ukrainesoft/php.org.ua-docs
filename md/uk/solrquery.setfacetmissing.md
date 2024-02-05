---
navigation:
  - solrquery.setfacetmincount.md: '« SolrQuery::setFacetMinCount'
  - solrquery.setfacetoffset.md: 'SolrQuery::setFacetOffset »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setFacetMissing'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setFacetMissing

(PECL solr >= 0.9.2)

SolrQuery::setFacetMissing — Відповідає facet.missing

### Опис

```methodsynopsis
public SolrQuery::setFacetMissing(bool $flag, string $field_override = ?): SolrQuery
```

Використовується для позначення того, що на додаток до обмежень поля фасету, що базуються на виразах, повинна бути обчислена кількість усіх результатів зіставлення, які не мають значення для поля.

### Список параметрів

`flag`

**`true`** включає цю функцію, **`false`** відключає її.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
