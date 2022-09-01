---
navigation:
  - solrcollapsefunction.sethint.html: '« SolrCollapseFunction::setHint'
  - solrcollapsefunction.setmin.html: 'SolrCollapseFunction::setMin »'
  - index.html: PHP Manual
  - class.solrcollapsefunction.html: SolrCollapseFunction
title: 'SolrCollapseFunction::setMax'
---
# SolrCollapseFunction::setMax

(PECL solr> = 2.2.0)

SolrCollapseFunction::setMax — Вибір заголовків групи за максимальним значенням числового поля або запитом функції

### Опис

```methodsynopsis
public SolrCollapseFunction::setMax(string $max): SolrCollapseFunction
```

Вибирає заголовки групи за максимальним значенням числового поля або запиту функції.

### Список параметрів

`max`

### Значення, що повертаються

[SolrCollapseFunction](class.solrcollapsefunction.html)

### Приклади

**Приклад #1 Приклад використання **SolrCollapseFunction::setMax()****

```php
<?php

$func = new SolrCollapseFunction('field_name');

$func->setMax('sum(cscore(),field(some_field))');

$query = new SolrQuery('*:*');

$query->collapse($func);

?>
```
